# Results vs. 3.12.6

- fork: nascheme
- ref: ft_float_consume_inp
- machine: linux-x86_64
- commit hash: ecf15ed
- commit date: 2025-02-05
- overall geometric mean: 1.044x slower
- HPT reliability: 99.93%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 302 ms: 1.15x slower                                                     |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                   |
| html5lib       | 63.6 ms                                                | 71.8 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                  | 1.11x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 575 ms: 1.93x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 603 ms: 1.80x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.76x faster                                                     |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.64x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 348 ms: 1.59x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 504 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 533 ms: 1.34x faster                                                     |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                     |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.2 ms: 1.06x faster                                                    |
| pidigits       | 184 ms                                                 | 198 ms: 1.08x slower                                                     |
| nbody          | 89.3 ms                                                | 130 ms: 1.46x slower                                                     |
| Geometric mean | (ref)                                                  | 1.14x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.13x faster                                                    |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                                     |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.0 ms: 1.17x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.0 ms: 1.10x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 2.34 sec: 1.11x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 246 us: 1.12x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 68.4 ms: 1.16x slower                                                    |
| json_loads           | 26.5 us                                                | 31.2 us: 1.18x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 367 us: 1.19x slower                                                     |
| json_dumps           | 10.4 ms                                                | 13.1 ms: 1.26x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.68 ms: 1.35x slower                                                    |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 58.9 ms: 1.17x slower                                                    |
| genshi_text     | 22.8 ms                                                | 27.8 ms: 1.22x slower                                                    |
| django_template | 34.7 ms                                                | 42.7 ms: 1.23x slower                                                    |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.67 ms: 2.07x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 575 ms: 1.93x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 603 ms: 1.80x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.76x faster                                                     |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.64x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 348 ms: 1.59x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 504 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 533 ms: 1.34x faster                                                     |
| pathlib                    | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                    |
| deepcopy                   | 352 us                                                 | 310 us: 1.14x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.13x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 88.0 ms: 1.10x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 37.5 us: 1.07x faster                                                    |
| float                      | 80.8 ms                                                | 76.2 ms: 1.06x faster                                                    |
| spectral_norm              | 110 ms                                                 | 105 ms: 1.04x faster                                                     |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                     |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.67 sec: 1.01x faster                                                   |
| go                         | 139 ms                                                 | 139 ms: 1.01x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                     |
| scimark_sor                | 130 ms                                                 | 131 ms: 1.01x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.15 us: 1.03x slower                                                    |
| dulwich_log                | 78.9 ms                                                | 81.6 ms: 1.04x slower                                                    |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                                     |
| logging_silent             | 109 ns                                                 | 115 ns: 1.05x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                   |
| json                       | 5.02 ms                                                | 5.40 ms: 1.07x slower                                                    |
| pidigits                   | 184 ms                                                 | 198 ms: 1.08x slower                                                     |
| raytrace                   | 299 ms                                                 | 325 ms: 1.09x slower                                                     |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 808 ms: 1.09x slower                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.67 sec: 1.10x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.28 us: 1.10x slower                                                    |
| chaos                      | 62.8 ms                                                | 69.4 ms: 1.10x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.2 ms: 1.11x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.34 sec: 1.11x slower                                                   |
| scimark_fft                | 342 ms                                                 | 380 ms: 1.11x slower                                                     |
| mdp                        | 2.42 sec                                               | 2.69 sec: 1.11x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 246 us: 1.12x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.12x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.13x slower                                                     |
| thrift                     | 791 us                                                 | 891 us: 1.13x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                    |
| html5lib                   | 63.6 ms                                                | 71.8 ms: 1.13x slower                                                    |
| logging_format             | 7.35 us                                                | 8.30 us: 1.13x slower                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 1.91 ms: 1.14x slower                                                    |
| pyflate                    | 448 ms                                                 | 512 ms: 1.14x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 61.0 ms: 1.15x slower                                                    |
| 2to3                       | 264 ms                                                 | 302 ms: 1.15x slower                                                     |
| sympy_str                  | 292 ms                                                 | 335 ms: 1.15x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 68.4 ms: 1.16x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 23.9 ms: 1.16x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 24.0 ms: 1.17x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.17x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 89.4 ms: 1.17x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.13 ms: 1.17x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 58.9 ms: 1.17x slower                                                    |
| sympy_expand               | 468 ms                                                 | 549 ms: 1.17x slower                                                     |
| json_loads                 | 26.5 us                                                | 31.2 us: 1.18x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 135 ms: 1.18x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 367 us: 1.19x slower                                                     |
| hexiom                     | 6.17 ms                                                | 7.37 ms: 1.19x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 81.9 ms: 1.20x slower                                                    |
| nqueens                    | 80.1 ms                                                | 96.5 ms: 1.20x slower                                                    |
| genshi_text                | 22.8 ms                                                | 27.8 ms: 1.22x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.22x slower                                                     |
| django_template            | 34.7 ms                                                | 42.7 ms: 1.23x slower                                                    |
| richards                   | 45.9 ms                                                | 56.6 ms: 1.23x slower                                                    |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 13.1 ms: 1.26x slower                                                    |
| richards_super             | 51.9 ms                                                | 65.8 ms: 1.27x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.40 ms: 1.29x slower                                                    |
| telco                      | 6.53 ms                                                | 8.57 ms: 1.31x slower                                                    |
| fannkuch                   | 372 ms                                                 | 491 ms: 1.32x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 9.68 ms: 1.35x slower                                                    |
| coverage                   | 71.4 ms                                                | 97.5 ms: 1.37x slower                                                    |
| deltablue                  | 3.45 ms                                                | 4.72 ms: 1.37x slower                                                    |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                    |
| nbody                      | 89.3 ms                                                | 130 ms: 1.46x slower                                                     |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.52x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 93.7 ms: 8.68x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                             |

Benchmark hidden because not significant (4): pylint, generators, pycparser, comprehensions
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250205-3.14.0a4+-ecf15ed-NOGIL/bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4+-ecf15ed.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.044x slower

# HPT report

- Reliability score: 99.93% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.35x