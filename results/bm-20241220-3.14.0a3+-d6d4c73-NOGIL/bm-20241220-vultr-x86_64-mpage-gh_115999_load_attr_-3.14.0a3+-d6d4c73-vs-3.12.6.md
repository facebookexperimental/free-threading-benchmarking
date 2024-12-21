# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: d6d4c73
- commit date: 2024-12-20
- overall geometric mean: 1.087x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 322 ms: 1.22x slower                                                  |
| docutils       | 2.64 sec                                               | 2.84 sec: 1.08x slower                                                |
| html5lib       | 63.6 ms                                                | 71.4 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 586 ms: 1.89x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                                  |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.64x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 484 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                  |
| async_generators           | 384 ms                                                 | 420 ms: 1.09x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| float          | 80.8 ms                                                | 81.9 ms: 1.01x slower                                                 |
| nbody          | 89.3 ms                                                | 136 ms: 1.52x slower                                                  |
| Geometric mean | (ref)                                                  | 1.15x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                 |
| regex_dna      | 168 ms                                                 | 177 ms: 1.06x slower                                                  |
| regex_compile  | 142 ms                                                 | 151 ms: 1.06x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.3 ms: 1.18x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.5 ms: 1.09x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| json_loads           | 26.5 us                                                | 27.9 us: 1.05x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 247 us: 1.12x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.8 ms: 1.14x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.6 ms: 1.16x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.49 sec: 1.18x slower                                                |
| pickle_pure_python   | 308 us                                                 | 370 us: 1.20x slower                                                  |
| json_dumps           | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                 |
| python_startup         | 9.93 ms                                                | 17.1 ms: 1.72x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.56x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.1 ms: 1.20x slower                                                 |
| django_template | 34.7 ms                                                | 42.9 ms: 1.24x slower                                                 |
| genshi_text     | 22.8 ms                                                | 28.5 ms: 1.25x slower                                                 |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 586 ms: 1.89x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                                  |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.64x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 484 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.12x faster                                                 |
| deepcopy                   | 352 us                                                 | 314 us: 1.12x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.5 ms: 1.09x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.07 us: 1.06x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 3.29 ms: 1.05x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 38.7 us: 1.04x faster                                                 |
| generators                 | 32.2 ms                                                | 31.3 ms: 1.03x faster                                                 |
| json                       | 5.02 ms                                                | 4.89 ms: 1.03x faster                                                 |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.79 sec: 1.01x slower                                                |
| float                      | 80.8 ms                                                | 81.9 ms: 1.01x slower                                                 |
| go                         | 139 ms                                                 | 143 ms: 1.03x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.22 sec: 1.04x slower                                                |
| spectral_norm              | 110 ms                                                 | 115 ms: 1.04x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 82.5 ms: 1.05x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.23 us: 1.05x slower                                                 |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                 |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.06x slower                                                  |
| comprehensions             | 19.8 us                                                | 21.0 us: 1.06x slower                                                 |
| regex_compile              | 142 ms                                                 | 151 ms: 1.06x slower                                                  |
| logging_silent             | 109 ns                                                 | 116 ns: 1.07x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.60 sec: 1.08x slower                                                |
| docutils                   | 2.64 sec                                               | 2.84 sec: 1.08x slower                                                |
| raytrace                   | 299 ms                                                 | 323 ms: 1.08x slower                                                  |
| pylint                     | 319 ms                                                 | 346 ms: 1.09x slower                                                  |
| async_generators           | 384 ms                                                 | 420 ms: 1.09x slower                                                  |
| pyflate                    | 448 ms                                                 | 497 ms: 1.11x slower                                                  |
| scimark_fft                | 342 ms                                                 | 380 ms: 1.11x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.4 ms: 1.12x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.42 us: 1.12x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 247 us: 1.12x slower                                                  |
| html5lib                   | 63.6 ms                                                | 71.4 ms: 1.12x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 841 ms: 1.13x slower                                                  |
| chaos                      | 62.8 ms                                                | 71.1 ms: 1.13x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 86.8 ms: 1.13x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.8 ms: 1.14x slower                                                 |
| logging_format             | 7.35 us                                                | 8.39 us: 1.14x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.74 sec: 1.15x slower                                                |
| sqlglot_optimize           | 53.3 ms                                                | 61.4 ms: 1.15x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 1.93 ms: 1.15x slower                                                 |
| thrift                     | 791 us                                                 | 915 us: 1.16x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.6 ms: 1.16x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.3 ms: 1.18x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.60 ms: 1.18x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.49 sec: 1.18x slower                                                |
| genshi_xml                 | 50.2 ms                                                | 60.1 ms: 1.20x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 370 us: 1.20x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                                  |
| nqueens                    | 80.1 ms                                                | 97.5 ms: 1.22x slower                                                 |
| 2to3                       | 264 ms                                                 | 322 ms: 1.22x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 176 ms: 1.23x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 84.5 ms: 1.23x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.62 ms: 1.23x slower                                                 |
| django_template            | 34.7 ms                                                | 42.9 ms: 1.24x slower                                                 |
| richards                   | 45.9 ms                                                | 56.9 ms: 1.24x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 142 ms: 1.24x slower                                                  |
| scimark_sor                | 130 ms                                                 | 162 ms: 1.25x slower                                                  |
| genshi_text                | 22.8 ms                                                | 28.5 ms: 1.25x slower                                                 |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                 |
| richards_super             | 51.9 ms                                                | 65.9 ms: 1.27x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.69 ms: 1.29x slower                                                 |
| telco                      | 6.53 ms                                                | 8.47 ms: 1.30x slower                                                 |
| fannkuch                   | 372 ms                                                 | 490 ms: 1.32x slower                                                  |
| coverage                   | 71.4 ms                                                | 99.3 ms: 1.39x slower                                                 |
| deltablue                  | 3.45 ms                                                | 4.84 ms: 1.40x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 28.9 ms: 1.40x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                 |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                 |
| nbody                      | 89.3 ms                                                | 136 ms: 1.52x slower                                                  |
| sympy_str                  | 292 ms                                                 | 459 ms: 1.58x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.79 ms: 1.64x slower                                                 |
| python_startup             | 9.93 ms                                                | 17.1 ms: 1.72x slower                                                 |
| sympy_expand               | 468 ms                                                 | 929 ms: 1.99x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 343 ms: 2.06x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.34 ms: 3.54x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 105 ms: 9.76x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.14x slower                                                          |

Benchmark hidden because not significant (1): coroutines
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241220-3.14.0a3+-d6d4c73-NOGIL/bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.087x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.34x