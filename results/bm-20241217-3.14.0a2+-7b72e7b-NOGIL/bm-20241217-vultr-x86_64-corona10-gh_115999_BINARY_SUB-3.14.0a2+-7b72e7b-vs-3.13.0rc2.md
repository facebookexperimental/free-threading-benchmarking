# Results vs. 3.13.0rc2

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 7b72e7b
- commit date: 2024-12-17
- overall geometric mean: 1.249x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 368 ms: 1.42x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.10 sec: 1.18x slower                                                   |
| html5lib       | 67.0 ms                                                      | 96.9 ms: 1.45x slower                                                    |
| Geometric mean | (ref)                                                        | 1.34x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 833 ms: 1.10x faster                                                     |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 649 ms: 1.03x faster                                                     |
| async_tree_io             | 876 ms                                                       | 855 ms: 1.03x faster                                                     |
| asyncio_websockets        | 520 ms                                                       | 518 ms: 1.00x faster                                                     |
| async_tree_memoization    | 461 ms                                                       | 473 ms: 1.03x slower                                                     |
| coroutines                | 23.6 ms                                                      | 24.4 ms: 1.03x slower                                                    |
| async_tree_none_tg        | 336 ms                                                       | 363 ms: 1.08x slower                                                     |
| async_tree_memoization_tg | 414 ms                                                       | 450 ms: 1.09x slower                                                     |
| async_tree_none           | 354 ms                                                       | 390 ms: 1.10x slower                                                     |
| async_generators          | 377 ms                                                       | 454 ms: 1.20x slower                                                     |
| Geometric mean            | (ref)                                                        | 1.03x slower                                                             |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.19x faster                                                     |
| nbody          | 85.1 ms                                                      | 131 ms: 1.53x slower                                                     |
| float          | 77.5 ms                                                      | 139 ms: 1.80x slower                                                     |
| Geometric mean | (ref)                                                        | 1.32x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                    |
| regex_dna      | 180 ms                                                       | 185 ms: 1.03x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 25.1 ms: 1.11x slower                                                    |
| regex_compile  | 132 ms                                                       | 178 ms: 1.35x slower                                                     |
| Geometric mean | (ref)                                                        | 1.09x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.4 ms: 1.04x faster                                                    |
| json_loads           | 27.0 us                                                      | 28.6 us: 1.06x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 97.5 ms: 1.14x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 78.2 ms: 1.32x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.67 sec: 1.33x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.3 ms: 1.35x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 335 us: 1.59x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 519 us: 1.76x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 65.1 ms: 1.34x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 32.0 ms: 1.48x slower                                                    |
| django_template | 34.1 ms                                                      | 51.6 ms: 1.51x slower                                                    |
| mako            | 11.3 ms                                                      | 17.9 ms: 1.57x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.47x slower                                                             |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 181 ms: 1.19x faster                                                     |
| async_tree_io_tg          | 913 ms                                                       | 833 ms: 1.10x faster                                                     |
| regex_effbot              | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                    |
| deepcopy                  | 355 us                                                       | 330 us: 1.08x faster                                                     |
| xml_etree_parse           | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| xml_etree_iterparse       | 94.9 ms                                                      | 91.4 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 649 ms: 1.03x faster                                                     |
| async_tree_io             | 876 ms                                                       | 855 ms: 1.03x faster                                                     |
| asyncio_websockets        | 520 ms                                                       | 518 ms: 1.00x faster                                                     |
| gc_traversal              | 3.14 ms                                                      | 3.21 ms: 1.02x slower                                                    |
| async_tree_memoization    | 461 ms                                                       | 473 ms: 1.03x slower                                                     |
| json                      | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                                    |
| regex_dna                 | 180 ms                                                       | 185 ms: 1.03x slower                                                     |
| deepcopy_memo             | 39.1 us                                                      | 40.2 us: 1.03x slower                                                    |
| coroutines                | 23.6 ms                                                      | 24.4 ms: 1.03x slower                                                    |
| sqlite_synth              | 2.21 us                                                      | 2.28 us: 1.03x slower                                                    |
| json_loads                | 27.0 us                                                      | 28.6 us: 1.06x slower                                                    |
| pathlib                   | 19.2 ms                                                      | 20.5 ms: 1.07x slower                                                    |
| async_tree_none_tg        | 336 ms                                                       | 363 ms: 1.08x slower                                                     |
| async_tree_memoization_tg | 414 ms                                                       | 450 ms: 1.09x slower                                                     |
| async_tree_none           | 354 ms                                                       | 390 ms: 1.10x slower                                                     |
| spectral_norm             | 111 ms                                                       | 123 ms: 1.11x slower                                                     |
| regex_v8                  | 22.7 ms                                                      | 25.1 ms: 1.11x slower                                                    |
| telco                     | 7.82 ms                                                      | 8.71 ms: 1.11x slower                                                    |
| bpe_tokeniser             | 4.45 sec                                                     | 5.00 sec: 1.13x slower                                                   |
| deepcopy_reduce           | 3.11 us                                                      | 3.55 us: 1.14x slower                                                    |
| xml_etree_generate        | 85.4 ms                                                      | 97.5 ms: 1.14x slower                                                    |
| scimark_fft               | 349 ms                                                       | 403 ms: 1.15x slower                                                     |
| mdp                       | 2.36 sec                                                     | 2.78 sec: 1.18x slower                                                   |
| docutils                  | 2.62 sec                                                     | 3.10 sec: 1.18x slower                                                   |
| coverage                  | 83.0 ms                                                      | 99.3 ms: 1.20x slower                                                    |
| async_generators          | 377 ms                                                       | 454 ms: 1.20x slower                                                     |
| pylint                    | 317 ms                                                       | 383 ms: 1.21x slower                                                     |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.80 ms: 1.23x slower                                                    |
| nqueens                   | 78.6 ms                                                      | 97.8 ms: 1.25x slower                                                    |
| dulwich_log               | 74.8 ms                                                      | 95.1 ms: 1.27x slower                                                    |
| meteor_contest            | 102 ms                                                       | 129 ms: 1.27x slower                                                     |
| typing_runtime_protocols  | 155 us                                                       | 200 us: 1.29x slower                                                     |
| sqlglot_normalize         | 106 ms                                                       | 137 ms: 1.30x slower                                                     |
| sqlglot_optimize          | 52.7 ms                                                      | 69.3 ms: 1.31x slower                                                    |
| xml_etree_process         | 59.3 ms                                                      | 78.2 ms: 1.32x slower                                                    |
| pprint_safe_repr          | 738 ms                                                       | 974 ms: 1.32x slower                                                     |
| tomli_loads               | 2.01 sec                                                     | 2.67 sec: 1.33x slower                                                   |
| genshi_xml                | 48.8 ms                                                      | 65.1 ms: 1.34x slower                                                    |
| pprint_pformat            | 1.50 sec                                                     | 2.01 sec: 1.34x slower                                                   |
| fannkuch                  | 370 ms                                                       | 497 ms: 1.34x slower                                                     |
| regex_compile             | 132 ms                                                       | 178 ms: 1.35x slower                                                     |
| create_gc_cycles          | 1.34 ms                                                      | 1.80 ms: 1.35x slower                                                    |
| json_dumps                | 10.5 ms                                                      | 14.3 ms: 1.35x slower                                                    |
| generators                | 28.8 ms                                                      | 39.0 ms: 1.35x slower                                                    |
| crypto_pyaes              | 67.9 ms                                                      | 92.9 ms: 1.37x slower                                                    |
| pycparser                 | 1.12 sec                                                     | 1.55 sec: 1.38x slower                                                   |
| python_startup_no_site    | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| scimark_lu                | 113 ms                                                       | 156 ms: 1.39x slower                                                     |
| 2to3                      | 260 ms                                                       | 368 ms: 1.42x slower                                                     |
| html5lib                  | 67.0 ms                                                      | 96.9 ms: 1.45x slower                                                    |
| genshi_text               | 21.5 ms                                                      | 32.0 ms: 1.48x slower                                                    |
| sympy_integrate           | 19.8 ms                                                      | 29.4 ms: 1.48x slower                                                    |
| thrift                    | 778 us                                                       | 1.16 ms: 1.49x slower                                                    |
| django_template           | 34.1 ms                                                      | 51.6 ms: 1.51x slower                                                    |
| nbody                     | 85.1 ms                                                      | 131 ms: 1.53x slower                                                     |
| pyflate                   | 449 ms                                                       | 699 ms: 1.56x slower                                                     |
| mako                      | 11.3 ms                                                      | 17.9 ms: 1.57x slower                                                    |
| python_startup            | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                    |
| unpickle_pure_python      | 210 us                                                       | 335 us: 1.59x slower                                                     |
| hexiom                    | 5.99 ms                                                      | 9.81 ms: 1.64x slower                                                    |
| comprehensions            | 16.5 us                                                      | 27.2 us: 1.66x slower                                                    |
| scimark_sor               | 134 ms                                                       | 225 ms: 1.68x slower                                                     |
| richards                  | 45.2 ms                                                      | 78.4 ms: 1.73x slower                                                    |
| sympy_str                 | 275 ms                                                       | 478 ms: 1.74x slower                                                     |
| richards_super            | 51.6 ms                                                      | 89.9 ms: 1.74x slower                                                    |
| logging_format            | 6.84 us                                                      | 12.0 us: 1.76x slower                                                    |
| pickle_pure_python        | 294 us                                                       | 519 us: 1.76x slower                                                     |
| logging_simple            | 6.16 us                                                      | 10.9 us: 1.77x slower                                                    |
| float                     | 77.5 ms                                                      | 139 ms: 1.80x slower                                                     |
| scimark_monte_carlo       | 65.4 ms                                                      | 119 ms: 1.82x slower                                                     |
| logging_silent            | 103 ns                                                       | 188 ns: 1.84x slower                                                     |
| chaos                     | 57.3 ms                                                      | 105 ms: 1.84x slower                                                     |
| sqlglot_transpile         | 1.56 ms                                                      | 3.00 ms: 1.92x slower                                                    |
| go                        | 141 ms                                                       | 274 ms: 1.95x slower                                                     |
| sqlglot_parse             | 1.25 ms                                                      | 2.59 ms: 2.07x slower                                                    |
| sympy_expand              | 457 ms                                                       | 958 ms: 2.10x slower                                                     |
| raytrace                  | 253 ms                                                       | 555 ms: 2.19x slower                                                     |
| sympy_sum                 | 156 ms                                                       | 350 ms: 2.25x slower                                                     |
| deltablue                 | 3.12 ms                                                      | 8.08 ms: 2.59x slower                                                    |
| bench_thread_pool         | 919 us                                                       | 3.42 ms: 3.72x slower                                                    |
| bench_mp_pool             | 11.0 ms                                                      | 109 ms: 9.91x slower                                                     |
| Geometric mean            | (ref)                                                        | 1.38x slower                                                             |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241217-3.14.0a2+-7b72e7b-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.249x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.24x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.31x