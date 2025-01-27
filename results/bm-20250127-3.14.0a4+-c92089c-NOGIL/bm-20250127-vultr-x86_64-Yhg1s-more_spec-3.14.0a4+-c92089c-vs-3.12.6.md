# Results vs. 3.12.6

- fork: Yhg1s
- ref: more_spec
- machine: linux-x86_64
- commit hash: c92089c
- commit date: 2025-01-27
- overall geometric mean: 1.062x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 307 ms: 1.17x slower                                       |
| docutils       | 2.64 sec                                               | 2.83 sec: 1.07x slower                                     |
| html5lib       | 63.6 ms                                                | 69.3 ms: 1.09x slower                                      |
| Geometric mean | (ref)                                                  | 1.11x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                       |
| async_tree_io              | 1.08 sec                                               | 616 ms: 1.76x faster                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                       |
| async_tree_none            | 464 ms                                                 | 293 ms: 1.58x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 360 ms: 1.54x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 511 ms: 1.41x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 544 ms: 1.31x faster                                       |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                       |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                      |
| Geometric mean             | (ref)                                                  | 1.42x faster                                               |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.7 ms: 1.05x faster                                      |
| pidigits       | 184 ms                                                 | 198 ms: 1.08x slower                                       |
| nbody          | 89.3 ms                                                | 131 ms: 1.46x slower                                       |
| Geometric mean | (ref)                                                  | 1.14x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.11x faster                                      |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                       |
| regex_dna      | 168 ms                                                 | 184 ms: 1.09x slower                                       |
| regex_v8       | 20.6 ms                                                | 24.2 ms: 1.18x slower                                      |
| Geometric mean | (ref)                                                  | 1.05x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.5 ms: 1.09x faster                                      |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                       |
| tomli_loads          | 2.11 sec                                               | 2.29 sec: 1.09x slower                                     |
| unpickle_pure_python | 221 us                                                 | 253 us: 1.15x slower                                       |
| xml_etree_generate   | 85.2 ms                                                | 98.3 ms: 1.15x slower                                      |
| json_loads           | 26.5 us                                                | 30.9 us: 1.16x slower                                      |
| xml_etree_process    | 59.0 ms                                                | 70.0 ms: 1.19x slower                                      |
| pickle_pure_python   | 308 us                                                 | 383 us: 1.24x slower                                       |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.25x slower                                      |
| Geometric mean       | (ref)                                                  | 1.11x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.54 ms: 1.33x slower                                      |
| python_startup         | 9.93 ms                                                | 15.2 ms: 1.53x slower                                      |
| Geometric mean         | (ref)                                                  | 1.43x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.4 ms: 1.20x slower                                      |
| genshi_text     | 22.8 ms                                                | 27.8 ms: 1.22x slower                                      |
| django_template | 34.7 ms                                                | 44.5 ms: 1.28x slower                                      |
| mako            | 11.0 ms                                                | 16.0 ms: 1.46x slower                                      |
| Geometric mean  | (ref)                                                  | 1.29x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                       |
| async_tree_io              | 1.08 sec                                               | 616 ms: 1.76x faster                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                       |
| async_tree_none            | 464 ms                                                 | 293 ms: 1.58x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 360 ms: 1.54x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 511 ms: 1.41x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 544 ms: 1.31x faster                                       |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.14x faster                                      |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.11x faster                                      |
| gc_traversal               | 3.46 ms                                                | 3.15 ms: 1.10x faster                                      |
| deepcopy                   | 352 us                                                 | 320 us: 1.10x faster                                       |
| xml_etree_iterparse        | 96.7 ms                                                | 88.5 ms: 1.09x faster                                      |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                       |
| sqlite_synth               | 2.20 us                                                | 2.08 us: 1.06x faster                                      |
| float                      | 80.8 ms                                                | 76.7 ms: 1.05x faster                                      |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                       |
| deepcopy_memo              | 40.3 us                                                | 39.4 us: 1.02x faster                                      |
| go                         | 139 ms                                                 | 140 ms: 1.00x slower                                       |
| scimark_sor                | 130 ms                                                 | 132 ms: 1.02x slower                                       |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                      |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.03x slower                                     |
| dulwich_log                | 78.9 ms                                                | 82.2 ms: 1.04x slower                                      |
| generators                 | 32.2 ms                                                | 33.8 ms: 1.05x slower                                      |
| comprehensions             | 19.8 us                                                | 20.9 us: 1.05x slower                                      |
| logging_silent             | 109 ns                                                 | 116 ns: 1.06x slower                                       |
| deepcopy_reduce            | 3.08 us                                                | 3.28 us: 1.07x slower                                      |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                       |
| docutils                   | 2.64 sec                                               | 2.83 sec: 1.07x slower                                     |
| json                       | 5.02 ms                                                | 5.39 ms: 1.07x slower                                      |
| pidigits                   | 184 ms                                                 | 198 ms: 1.08x slower                                       |
| mdp                        | 2.42 sec                                               | 2.60 sec: 1.08x slower                                     |
| tomli_loads                | 2.11 sec                                               | 2.29 sec: 1.09x slower                                     |
| html5lib                   | 63.6 ms                                                | 69.3 ms: 1.09x slower                                      |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.09x slower                                       |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.9 ms: 1.10x slower                                      |
| pyflate                    | 448 ms                                                 | 493 ms: 1.10x slower                                       |
| chaos                      | 62.8 ms                                                | 69.4 ms: 1.11x slower                                      |
| raytrace                   | 299 ms                                                 | 331 ms: 1.11x slower                                       |
| logging_simple             | 6.63 us                                                | 7.33 us: 1.11x slower                                      |
| scimark_fft                | 342 ms                                                 | 379 ms: 1.11x slower                                       |
| pprint_safe_repr           | 743 ms                                                 | 830 ms: 1.12x slower                                       |
| logging_format             | 7.35 us                                                | 8.26 us: 1.12x slower                                      |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                       |
| crypto_pyaes               | 76.6 ms                                                | 86.6 ms: 1.13x slower                                      |
| pprint_pformat             | 1.52 sec                                               | 1.72 sec: 1.13x slower                                     |
| sqlglot_transpile          | 1.67 ms                                                | 1.91 ms: 1.15x slower                                      |
| unpickle_pure_python       | 221 us                                                 | 253 us: 1.15x slower                                       |
| sqlalchemy_declarative     | 143 ms                                                 | 164 ms: 1.15x slower                                       |
| sqlglot_normalize          | 107 ms                                                 | 122 ms: 1.15x slower                                       |
| xml_etree_generate         | 85.2 ms                                                | 98.3 ms: 1.15x slower                                      |
| sympy_str                  | 292 ms                                                 | 337 ms: 1.16x slower                                       |
| json_loads                 | 26.5 us                                                | 30.9 us: 1.16x slower                                      |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.17x slower                                      |
| 2to3                       | 264 ms                                                 | 307 ms: 1.17x slower                                       |
| sqlglot_optimize           | 53.3 ms                                                | 62.1 ms: 1.17x slower                                      |
| sympy_expand               | 468 ms                                                 | 550 ms: 1.18x slower                                       |
| regex_v8                   | 20.6 ms                                                | 24.2 ms: 1.18x slower                                      |
| thrift                     | 791 us                                                 | 933 us: 1.18x slower                                       |
| sympy_integrate            | 20.5 ms                                                | 24.4 ms: 1.19x slower                                      |
| xml_etree_process          | 59.0 ms                                                | 70.0 ms: 1.19x slower                                      |
| hexiom                     | 6.17 ms                                                | 7.37 ms: 1.20x slower                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 82.3 ms: 1.20x slower                                      |
| scimark_lu                 | 114 ms                                                 | 137 ms: 1.20x slower                                       |
| genshi_xml                 | 50.2 ms                                                | 60.4 ms: 1.20x slower                                      |
| nqueens                    | 80.1 ms                                                | 97.6 ms: 1.22x slower                                      |
| genshi_text                | 22.8 ms                                                | 27.8 ms: 1.22x slower                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.22x slower                                      |
| richards                   | 45.9 ms                                                | 57.1 ms: 1.24x slower                                      |
| pickle_pure_python         | 308 us                                                 | 383 us: 1.24x slower                                       |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.47 ms: 1.24x slower                                      |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.25x slower                                      |
| typing_runtime_protocols   | 163 us                                                 | 206 us: 1.26x slower                                       |
| meteor_contest             | 104 ms                                                 | 132 ms: 1.28x slower                                       |
| django_template            | 34.7 ms                                                | 44.5 ms: 1.28x slower                                      |
| richards_super             | 51.9 ms                                                | 66.9 ms: 1.29x slower                                      |
| fannkuch                   | 372 ms                                                 | 481 ms: 1.29x slower                                       |
| telco                      | 6.53 ms                                                | 8.61 ms: 1.32x slower                                      |
| python_startup_no_site     | 7.16 ms                                                | 9.54 ms: 1.33x slower                                      |
| coverage                   | 71.4 ms                                                | 96.6 ms: 1.35x slower                                      |
| deltablue                  | 3.45 ms                                                | 4.69 ms: 1.36x slower                                      |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.46x slower                                      |
| nbody                      | 89.3 ms                                                | 131 ms: 1.46x slower                                       |
| python_startup             | 9.93 ms                                                | 15.2 ms: 1.53x slower                                      |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.52x slower                                      |
| bench_mp_pool              | 10.8 ms                                                | 94.4 ms: 8.75x slower                                      |
| Geometric mean             | (ref)                                                  | 1.11x slower                                               |

Benchmark hidden because not significant (4): asyncio_websockets, spectral_norm, bpe_tokeniser, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250127-3.14.0a4+-c92089c-NOGIL/bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4+-c92089c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.062x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.36x