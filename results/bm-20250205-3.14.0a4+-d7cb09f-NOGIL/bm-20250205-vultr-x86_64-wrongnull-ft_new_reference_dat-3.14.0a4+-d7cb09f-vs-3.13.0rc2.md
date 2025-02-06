# Results vs. 3.13.0rc2

- fork: wrongnull
- ref: ft_new_reference_dat
- machine: linux-x86_64
- commit hash: d7cb09f
- commit date: 2025-02-05
- overall geometric mean: 1.073x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 302 ms: 1.16x slower                                                      |
| docutils       | 2.62 sec                                                     | 2.78 sec: 1.06x slower                                                    |
| html5lib       | 67.0 ms                                                      | 71.0 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                        | 1.09x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 570 ms: 1.60x faster                                                      |
| async_tree_io              | 876 ms                                                       | 600 ms: 1.46x faster                                                      |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                      |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 503 ms: 1.27x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 535 ms: 1.25x faster                                                      |
| async_tree_none            | 354 ms                                                       | 285 ms: 1.24x faster                                                      |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.01x faster                                                      |
| coroutines                 | 23.6 ms                                                      | 23.6 ms: 1.00x slower                                                     |
| async_generators           | 377 ms                                                       | 379 ms: 1.00x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.13x faster                                                      |
| float          | 77.5 ms                                                      | 75.9 ms: 1.02x faster                                                     |
| nbody          | 85.1 ms                                                      | 132 ms: 1.55x slower                                                      |
| Geometric mean | (ref)                                                        | 1.10x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.84 ms: 1.08x faster                                                     |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                      |
| regex_v8       | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                     |
| regex_compile  | 132 ms                                                       | 150 ms: 1.14x slower                                                      |
| Geometric mean | (ref)                                                        | 1.02x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.2 ms: 1.09x faster                                                     |
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                      |
| xml_etree_generate   | 85.4 ms                                                      | 95.5 ms: 1.12x slower                                                     |
| xml_etree_process    | 59.3 ms                                                      | 68.0 ms: 1.15x slower                                                     |
| json_loads           | 27.0 us                                                      | 31.1 us: 1.15x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 245 us: 1.17x slower                                                      |
| json_dumps           | 10.5 ms                                                      | 12.8 ms: 1.21x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 366 us: 1.24x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.65 ms: 1.31x slower                                                     |
| python_startup         | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 58.0 ms: 1.19x slower                                                     |
| django_template | 34.1 ms                                                      | 41.3 ms: 1.21x slower                                                     |
| genshi_text     | 21.5 ms                                                      | 27.3 ms: 1.27x slower                                                     |
| mako            | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.26x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.67 ms: 1.88x faster                                                     |
| async_tree_io_tg           | 913 ms                                                       | 570 ms: 1.60x faster                                                      |
| async_tree_io              | 876 ms                                                       | 600 ms: 1.46x faster                                                      |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                      |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 503 ms: 1.27x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 535 ms: 1.25x faster                                                      |
| async_tree_none            | 354 ms                                                       | 285 ms: 1.24x faster                                                      |
| deepcopy                   | 355 us                                                       | 307 us: 1.16x faster                                                      |
| pidigits                   | 217 ms                                                       | 191 ms: 1.13x faster                                                      |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.2 ms: 1.09x faster                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.03 us: 1.09x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.84 ms: 1.08x faster                                                     |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                      |
| pathlib                    | 19.2 ms                                                      | 18.4 ms: 1.04x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 37.9 us: 1.03x faster                                                     |
| float                      | 77.5 ms                                                      | 75.9 ms: 1.02x faster                                                     |
| scimark_sor                | 134 ms                                                       | 133 ms: 1.01x faster                                                      |
| go                         | 141 ms                                                       | 139 ms: 1.01x faster                                                      |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.01x faster                                                      |
| spectral_norm              | 111 ms                                                       | 111 ms: 1.00x faster                                                      |
| coroutines                 | 23.6 ms                                                      | 23.6 ms: 1.00x slower                                                     |
| async_generators           | 377 ms                                                       | 379 ms: 1.00x slower                                                      |
| deepcopy_reduce            | 3.11 us                                                      | 3.13 us: 1.01x slower                                                     |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                      |
| regex_v8                   | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.62 sec: 1.04x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.05x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.40 ms: 1.05x slower                                                     |
| html5lib                   | 67.0 ms                                                      | 71.0 ms: 1.06x slower                                                     |
| docutils                   | 2.62 sec                                                     | 2.78 sec: 1.06x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 794 ms: 1.08x slower                                                      |
| logging_silent             | 103 ns                                                       | 111 ns: 1.08x slower                                                      |
| json                       | 4.93 ms                                                      | 5.36 ms: 1.09x slower                                                     |
| mdp                        | 2.36 sec                                                     | 2.57 sec: 1.09x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 82.0 ms: 1.10x slower                                                     |
| telco                      | 7.82 ms                                                      | 8.60 ms: 1.10x slower                                                     |
| pprint_pformat             | 1.50 sec                                                     | 1.65 sec: 1.10x slower                                                    |
| scimark_fft                | 349 ms                                                       | 384 ms: 1.10x slower                                                      |
| generators                 | 28.8 ms                                                      | 31.8 ms: 1.10x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 95.5 ms: 1.12x slower                                                     |
| pyflate                    | 449 ms                                                       | 504 ms: 1.12x slower                                                      |
| sqlglot_normalize          | 106 ms                                                       | 119 ms: 1.13x slower                                                      |
| regex_compile              | 132 ms                                                       | 150 ms: 1.14x slower                                                      |
| xml_etree_process          | 59.3 ms                                                      | 68.0 ms: 1.15x slower                                                     |
| thrift                     | 778 us                                                       | 893 us: 1.15x slower                                                      |
| sqlglot_optimize           | 52.7 ms                                                      | 60.6 ms: 1.15x slower                                                     |
| json_loads                 | 27.0 us                                                      | 31.1 us: 1.15x slower                                                     |
| logging_simple             | 6.16 us                                                      | 7.15 us: 1.16x slower                                                     |
| 2to3                       | 260 ms                                                       | 302 ms: 1.16x slower                                                      |
| tomli_loads                | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 245 us: 1.17x slower                                                      |
| coverage                   | 83.0 ms                                                      | 97.0 ms: 1.17x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 58.0 ms: 1.19x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 185 ms: 1.19x slower                                                      |
| sympy_expand               | 457 ms                                                       | 545 ms: 1.19x slower                                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.62 ms: 1.19x slower                                                     |
| logging_format             | 6.84 us                                                      | 8.21 us: 1.20x slower                                                     |
| comprehensions             | 16.5 us                                                      | 19.8 us: 1.20x slower                                                     |
| sympy_integrate            | 19.8 ms                                                      | 24.0 ms: 1.21x slower                                                     |
| django_template            | 34.1 ms                                                      | 41.3 ms: 1.21x slower                                                     |
| sympy_str                  | 275 ms                                                       | 333 ms: 1.21x slower                                                      |
| sqlglot_transpile          | 1.56 ms                                                      | 1.89 ms: 1.21x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 12.8 ms: 1.21x slower                                                     |
| scimark_lu                 | 113 ms                                                       | 137 ms: 1.22x slower                                                      |
| nqueens                    | 78.6 ms                                                      | 95.9 ms: 1.22x slower                                                     |
| chaos                      | 57.3 ms                                                      | 70.1 ms: 1.22x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 7.39 ms: 1.23x slower                                                     |
| pickle_pure_python         | 294 us                                                       | 366 us: 1.24x slower                                                      |
| richards                   | 45.2 ms                                                      | 56.5 ms: 1.25x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                      | 1.57 ms: 1.25x slower                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 82.1 ms: 1.26x slower                                                     |
| genshi_text                | 21.5 ms                                                      | 27.3 ms: 1.27x slower                                                     |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                      |
| richards_super             | 51.6 ms                                                      | 65.7 ms: 1.27x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 198 us: 1.28x slower                                                      |
| raytrace                   | 253 ms                                                       | 328 ms: 1.30x slower                                                      |
| python_startup_no_site     | 7.39 ms                                                      | 9.65 ms: 1.31x slower                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 89.6 ms: 1.32x slower                                                     |
| fannkuch                   | 370 ms                                                       | 491 ms: 1.33x slower                                                      |
| mako                       | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                     |
| python_startup             | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 4.67 ms: 1.50x slower                                                     |
| nbody                      | 85.1 ms                                                      | 132 ms: 1.55x slower                                                      |
| bench_thread_pool          | 919 us                                                       | 3.30 ms: 3.59x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                      | 93.8 ms: 8.53x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.12x slower                                                              |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250205-3.14.0a4+-d7cb09f-NOGIL/bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.073x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x