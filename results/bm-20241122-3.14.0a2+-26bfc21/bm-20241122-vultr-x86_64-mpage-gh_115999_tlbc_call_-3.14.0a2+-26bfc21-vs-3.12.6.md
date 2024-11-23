# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: 26bfc21
- commit date: 2024-11-22
- overall geometric mean: 1.01x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 256 ms: 1.03x faster                                                  |
| html5lib       | 63.6 ms                                                | 67.0 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 390 ms: 1.44x faster                                                  |
| async_tree_none            | 464 ms                                                 | 334 ms: 1.39x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 407 ms: 1.36x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 344 ms: 1.30x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 843 ms: 1.28x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 888 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 630 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 628 ms: 1.14x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.07x faster                                                 |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 89.3 ms                                                | 94.9 ms: 1.06x slower                                                 |
| pidigits       | 184 ms                                                 | 216 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                 |
| regex_compile  | 142 ms                                                 | 136 ms: 1.05x faster                                                  |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.4 ms: 1.18x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_loads           | 26.5 us                                                | 25.0 us: 1.06x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 214 us: 1.03x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 137 ms: 1.02x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                |
| xml_etree_generate   | 85.2 ms                                                | 86.7 ms: 1.02x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 60.3 ms: 1.02x slower                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 98.9 ms: 1.02x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 318 us: 1.03x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.39 ms: 1.03x slower                                                 |
| python_startup         | 9.93 ms                                                | 13.2 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.9 ms: 1.04x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 49.8 ms: 1.01x faster                                                 |
| django_template | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                 |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 390 ms: 1.44x faster                                                  |
| async_tree_none            | 464 ms                                                 | 334 ms: 1.39x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 407 ms: 1.36x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.6 us: 1.36x faster                                                 |
| deepcopy                   | 352 us                                                 | 258 us: 1.36x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 344 ms: 1.30x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 843 ms: 1.28x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 888 ms: 1.25x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.58 us: 1.19x faster                                                 |
| pylint                     | 319 ms                                                 | 270 ms: 1.18x faster                                                  |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.4 ms: 1.17x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.3 us: 1.15x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 630 ms: 1.15x faster                                                  |
| raytrace                   | 299 ms                                                 | 262 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 628 ms: 1.14x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 67.7 ms: 1.13x faster                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.13x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.5 ms: 1.12x faster                                                 |
| json                       | 5.02 ms                                                | 4.51 ms: 1.11x faster                                                 |
| generators                 | 32.2 ms                                                | 29.3 ms: 1.10x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                 |
| chaos                      | 62.8 ms                                                | 58.3 ms: 1.08x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.41 sec: 1.07x faster                                                |
| logging_simple             | 6.63 us                                                | 6.18 us: 1.07x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.23 ms: 1.07x faster                                                 |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.07x faster                                                 |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.06x faster                                                  |
| json_loads                 | 26.5 us                                                | 25.0 us: 1.06x faster                                                 |
| logging_format             | 7.35 us                                                | 6.94 us: 1.06x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 64.9 ms: 1.05x faster                                                 |
| thrift                     | 791 us                                                 | 753 us: 1.05x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                 |
| regex_compile              | 142 ms                                                 | 136 ms: 1.05x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.60 ms: 1.05x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.45 sec: 1.05x faster                                                |
| genshi_text                | 22.8 ms                                                | 21.9 ms: 1.04x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 713 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                |
| dulwich_log                | 78.9 ms                                                | 76.4 ms: 1.03x faster                                                 |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.98 ms: 1.03x faster                                                 |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 214 us: 1.03x faster                                                  |
| 2to3                       | 264 ms                                                 | 256 ms: 1.03x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.03x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 20.0 ms: 1.03x faster                                                 |
| logging_silent             | 109 ns                                                 | 106 ns: 1.02x faster                                                  |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 137 ms: 1.02x faster                                                  |
| scimark_fft                | 342 ms                                                 | 337 ms: 1.01x faster                                                  |
| sympy_expand               | 468 ms                                                 | 461 ms: 1.01x faster                                                  |
| nqueens                    | 80.1 ms                                                | 79.0 ms: 1.01x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                |
| genshi_xml                 | 50.2 ms                                                | 49.8 ms: 1.01x faster                                                 |
| fannkuch                   | 372 ms                                                 | 371 ms: 1.00x faster                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 53.6 ms: 1.01x slower                                                 |
| richards_super             | 51.9 ms                                                | 52.5 ms: 1.01x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                  |
| richards                   | 45.9 ms                                                | 46.6 ms: 1.01x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 86.7 ms: 1.02x slower                                                 |
| django_template            | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 60.3 ms: 1.02x slower                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 98.9 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.51 ms: 1.03x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.49 sec: 1.03x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 7.39 ms: 1.03x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 318 us: 1.03x slower                                                  |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.03x slower                                                  |
| html5lib                   | 63.6 ms                                                | 67.0 ms: 1.05x slower                                                 |
| nbody                      | 89.3 ms                                                | 94.9 ms: 1.06x slower                                                 |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.08x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                 |
| regex_dna                  | 168 ms                                                 | 186 ms: 1.11x slower                                                  |
| telco                      | 6.53 ms                                                | 7.25 ms: 1.11x slower                                                 |
| coverage                   | 71.4 ms                                                | 80.7 ms: 1.13x slower                                                 |
| pidigits                   | 184 ms                                                 | 216 ms: 1.17x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.4 ms: 1.18x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.22 ms: 1.22x slower                                                 |
| python_startup             | 9.93 ms                                                | 13.2 ms: 1.33x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.91 ms: 1.75x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 86.1 ms: 7.97x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (5): float, docutils, sqlglot_normalize, pyflate, sqlite_synth
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241122-3.14.0a2+-26bfc21/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x