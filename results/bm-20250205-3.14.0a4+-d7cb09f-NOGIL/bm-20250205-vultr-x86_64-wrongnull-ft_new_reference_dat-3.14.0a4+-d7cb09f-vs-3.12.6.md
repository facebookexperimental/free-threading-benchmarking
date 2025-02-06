# Results vs. 3.12.6

- fork: wrongnull
- ref: ft_new_reference_dat
- machine: linux-x86_64
- commit hash: d7cb09f
- commit date: 2025-02-05
- overall geometric mean: 1.042x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 302 ms: 1.14x slower                                                      |
| docutils       | 2.64 sec                                               | 2.78 sec: 1.05x slower                                                    |
| html5lib       | 63.6 ms                                                | 71.0 ms: 1.12x slower                                                     |
| Geometric mean | (ref)                                                  | 1.10x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 570 ms: 1.95x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.80x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 600 ms: 1.80x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                      |
| async_tree_none            | 464 ms                                                 | 285 ms: 1.63x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 503 ms: 1.44x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 535 ms: 1.34x faster                                                      |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                     |
| async_generators           | 384 ms                                                 | 379 ms: 1.01x faster                                                      |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.9 ms: 1.06x faster                                                     |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                      |
| nbody          | 89.3 ms                                                | 132 ms: 1.48x slower                                                      |
| Geometric mean | (ref)                                                  | 1.13x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                     |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                                      |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                                      |
| regex_v8       | 20.6 ms                                                | 23.2 ms: 1.13x slower                                                     |
| Geometric mean | (ref)                                                  | 1.04x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.2 ms: 1.11x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                      |
| tomli_loads          | 2.11 sec                                               | 2.34 sec: 1.11x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 245 us: 1.11x slower                                                      |
| xml_etree_generate   | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                     |
| xml_etree_process    | 59.0 ms                                                | 68.0 ms: 1.15x slower                                                     |
| json_loads           | 26.5 us                                                | 31.1 us: 1.17x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 366 us: 1.19x slower                                                      |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.23x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.65 ms: 1.35x slower                                                     |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 58.0 ms: 1.16x slower                                                     |
| django_template | 34.7 ms                                                | 41.3 ms: 1.19x slower                                                     |
| genshi_text     | 22.8 ms                                                | 27.3 ms: 1.20x slower                                                     |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.24x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.67 ms: 2.07x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 570 ms: 1.95x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.80x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 600 ms: 1.80x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                      |
| async_tree_none            | 464 ms                                                 | 285 ms: 1.63x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 503 ms: 1.44x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 535 ms: 1.34x faster                                                      |
| pathlib                    | 21.5 ms                                                | 18.4 ms: 1.17x faster                                                     |
| deepcopy                   | 352 us                                                 | 307 us: 1.15x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 87.2 ms: 1.11x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                      |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                     |
| float                      | 80.8 ms                                                | 75.9 ms: 1.06x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 37.9 us: 1.06x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.62 sec: 1.03x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                     |
| async_generators           | 384 ms                                                 | 379 ms: 1.01x faster                                                      |
| generators                 | 32.2 ms                                                | 31.8 ms: 1.01x faster                                                     |
| comprehensions             | 19.8 us                                                | 19.8 us: 1.00x faster                                                     |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.00x slower                                                      |
| deepcopy_reduce            | 3.08 us                                                | 3.13 us: 1.02x slower                                                     |
| logging_silent             | 109 ns                                                 | 111 ns: 1.02x slower                                                      |
| scimark_sor                | 130 ms                                                 | 133 ms: 1.02x slower                                                      |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                      |
| dulwich_log                | 78.9 ms                                                | 82.0 ms: 1.04x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.78 sec: 1.05x slower                                                    |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                                      |
| mdp                        | 2.42 sec                                               | 2.57 sec: 1.06x slower                                                    |
| json                       | 5.02 ms                                                | 5.36 ms: 1.07x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 794 ms: 1.07x slower                                                      |
| logging_simple             | 6.63 us                                                | 7.15 us: 1.08x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.65 sec: 1.08x slower                                                    |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                                      |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                                      |
| raytrace                   | 299 ms                                                 | 328 ms: 1.10x slower                                                      |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.0 ms: 1.10x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.34 sec: 1.11x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 245 us: 1.11x slower                                                      |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.12x slower                                                      |
| html5lib                   | 63.6 ms                                                | 71.0 ms: 1.12x slower                                                     |
| chaos                      | 62.8 ms                                                | 70.1 ms: 1.12x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 119 ms: 1.12x slower                                                      |
| logging_format             | 7.35 us                                                | 8.21 us: 1.12x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                     |
| scimark_fft                | 342 ms                                                 | 384 ms: 1.13x slower                                                      |
| pyflate                    | 448 ms                                                 | 504 ms: 1.13x slower                                                      |
| regex_v8                   | 20.6 ms                                                | 23.2 ms: 1.13x slower                                                     |
| thrift                     | 791 us                                                 | 893 us: 1.13x slower                                                      |
| sqlglot_transpile          | 1.67 ms                                                | 1.89 ms: 1.13x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 60.6 ms: 1.14x slower                                                     |
| sympy_str                  | 292 ms                                                 | 333 ms: 1.14x slower                                                      |
| 2to3                       | 264 ms                                                 | 302 ms: 1.14x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 68.0 ms: 1.15x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 1.57 ms: 1.16x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 58.0 ms: 1.16x slower                                                     |
| sympy_expand               | 468 ms                                                 | 545 ms: 1.17x slower                                                      |
| sympy_integrate            | 20.5 ms                                                | 24.0 ms: 1.17x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 89.6 ms: 1.17x slower                                                     |
| json_loads                 | 26.5 us                                                | 31.1 us: 1.17x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 366 us: 1.19x slower                                                      |
| django_template            | 34.7 ms                                                | 41.3 ms: 1.19x slower                                                     |
| genshi_text                | 22.8 ms                                                | 27.3 ms: 1.20x slower                                                     |
| nqueens                    | 80.1 ms                                                | 95.9 ms: 1.20x slower                                                     |
| hexiom                     | 6.17 ms                                                | 7.39 ms: 1.20x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 82.1 ms: 1.20x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 137 ms: 1.20x slower                                                      |
| typing_runtime_protocols   | 163 us                                                 | 198 us: 1.21x slower                                                      |
| richards                   | 45.9 ms                                                | 56.5 ms: 1.23x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.23x slower                                                     |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                      |
| richards_super             | 51.9 ms                                                | 65.7 ms: 1.27x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.62 ms: 1.28x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.40 ms: 1.29x slower                                                     |
| telco                      | 6.53 ms                                                | 8.60 ms: 1.32x slower                                                     |
| fannkuch                   | 372 ms                                                 | 491 ms: 1.32x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 9.65 ms: 1.35x slower                                                     |
| deltablue                  | 3.45 ms                                                | 4.67 ms: 1.36x slower                                                     |
| coverage                   | 71.4 ms                                                | 97.0 ms: 1.36x slower                                                     |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                     |
| nbody                      | 89.3 ms                                                | 132 ms: 1.48x slower                                                      |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 3.30 ms: 3.51x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 93.8 ms: 8.69x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                              |

Benchmark hidden because not significant (4): pylint, go, asyncio_websockets, pycparser
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250205-3.14.0a4+-d7cb09f-NOGIL/bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.042x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.35x