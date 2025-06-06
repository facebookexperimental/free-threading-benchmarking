# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: e517ccb
- commit date: 2024-12-02
- overall geometric mean: 1.030x faster
- HPT reliability: 99.23%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 259 ms: 1.02x faster                                                     |
| docutils       | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 392 ms: 1.43x faster                                                     |
| async_tree_none            | 464 ms                                                 | 334 ms: 1.39x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 409 ms: 1.36x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 347 ms: 1.29x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 851 ms: 1.27x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 892 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 632 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 635 ms: 1.13x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                    |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 82.1 ms: 1.02x slower                                                    |
| nbody          | 89.3 ms                                                | 94.9 ms: 1.06x slower                                                    |
| pidigits       | 184 ms                                                 | 216 ms: 1.18x slower                                                     |
| Geometric mean | (ref)                                                  | 1.08x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                    |
| regex_compile  | 142 ms                                                 | 130 ms: 1.09x faster                                                     |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                    |
| Geometric mean | (ref)                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 26.5 us                                                | 24.9 us: 1.07x faster                                                    |
| unpickle_pure_python | 221 us                                                 | 217 us: 1.02x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 138 ms: 1.01x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 2.13 sec: 1.01x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 86.7 ms: 1.02x slower                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 98.7 ms: 1.02x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 61.0 ms: 1.03x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 323 us: 1.05x slower                                                     |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                    |
| python_startup         | 9.93 ms                                                | 14.5 ms: 1.46x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                    |
| django_template | 34.7 ms                                                | 35.7 ms: 1.03x slower                                                    |
| mako            | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 392 ms: 1.43x faster                                                     |
| async_tree_none            | 464 ms                                                 | 334 ms: 1.39x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 409 ms: 1.36x faster                                                     |
| deepcopy                   | 352 us                                                 | 263 us: 1.34x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 31.2 us: 1.29x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 347 ms: 1.29x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 851 ms: 1.27x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 892 ms: 1.24x faster                                                     |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                    |
| pylint                     | 319 ms                                                 | 271 ms: 1.18x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.63 us: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 632 ms: 1.14x faster                                                     |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                     |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 635 ms: 1.13x faster                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.13x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                    |
| raytrace                   | 299 ms                                                 | 268 ms: 1.12x faster                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.5 ms: 1.12x faster                                                    |
| json                       | 5.02 ms                                                | 4.52 ms: 1.11x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 69.4 ms: 1.10x faster                                                    |
| generators                 | 32.2 ms                                                | 29.4 ms: 1.10x faster                                                    |
| regex_compile              | 142 ms                                                 | 130 ms: 1.09x faster                                                     |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.44 sec: 1.07x faster                                                   |
| json_loads                 | 26.5 us                                                | 24.9 us: 1.07x faster                                                    |
| thrift                     | 791 us                                                 | 744 us: 1.06x faster                                                     |
| chaos                      | 62.8 ms                                                | 59.1 ms: 1.06x faster                                                    |
| sympy_str                  | 292 ms                                                 | 275 ms: 1.06x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                    |
| logging_simple             | 6.63 us                                                | 6.28 us: 1.06x faster                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 1.61 ms: 1.04x faster                                                    |
| deltablue                  | 3.45 ms                                                | 3.32 ms: 1.04x faster                                                    |
| logging_format             | 7.35 us                                                | 7.08 us: 1.04x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 76.1 ms: 1.04x faster                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 66.0 ms: 1.04x faster                                                    |
| sqlglot_parse              | 1.36 ms                                                | 1.31 ms: 1.04x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                   |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.48 sec: 1.03x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.02x faster                                                     |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.02x faster                                                     |
| sympy_integrate            | 20.5 ms                                                | 20.1 ms: 1.02x faster                                                    |
| hexiom                     | 6.17 ms                                                | 6.04 ms: 1.02x faster                                                    |
| genshi_text                | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 729 ms: 1.02x faster                                                     |
| 2to3                       | 264 ms                                                 | 259 ms: 1.02x faster                                                     |
| unpickle_pure_python       | 221 us                                                 | 217 us: 1.02x faster                                                     |
| sympy_expand               | 468 ms                                                 | 462 ms: 1.01x faster                                                     |
| scimark_lu                 | 114 ms                                                 | 113 ms: 1.01x faster                                                     |
| docutils                   | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 138 ms: 1.01x faster                                                     |
| nqueens                    | 80.1 ms                                                | 79.6 ms: 1.01x faster                                                    |
| pyflate                    | 448 ms                                                 | 453 ms: 1.01x slower                                                     |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| logging_silent             | 109 ns                                                 | 110 ns: 1.01x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.13 sec: 1.01x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 108 ms: 1.01x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 54.1 ms: 1.02x slower                                                    |
| float                      | 80.8 ms                                                | 82.1 ms: 1.02x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 86.7 ms: 1.02x slower                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 98.7 ms: 1.02x slower                                                    |
| richards                   | 45.9 ms                                                | 47.1 ms: 1.03x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 7.36 ms: 1.03x slower                                                    |
| django_template            | 34.7 ms                                                | 35.7 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.53 ms: 1.03x slower                                                    |
| richards_super             | 51.9 ms                                                | 53.5 ms: 1.03x slower                                                    |
| mdp                        | 2.42 sec                                               | 2.50 sec: 1.03x slower                                                   |
| fannkuch                   | 372 ms                                                 | 385 ms: 1.03x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 61.0 ms: 1.03x slower                                                    |
| scimark_sor                | 130 ms                                                 | 135 ms: 1.04x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 323 us: 1.05x slower                                                     |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                     |
| spectral_norm              | 110 ms                                                 | 117 ms: 1.06x slower                                                     |
| nbody                      | 89.3 ms                                                | 94.9 ms: 1.06x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.09x slower                                                    |
| mako                       | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                    |
| coverage                   | 71.4 ms                                                | 79.3 ms: 1.11x slower                                                    |
| telco                      | 6.53 ms                                                | 7.33 ms: 1.12x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 3.94 ms: 1.14x slower                                                    |
| pidigits                   | 184 ms                                                 | 216 ms: 1.18x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                    |
| python_startup             | 9.93 ms                                                | 14.5 ms: 1.46x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.77x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 85.8 ms: 7.95x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (3): genshi_xml, scimark_fft, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241202-3.14.0a2+-e517ccb/bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.030x faster

# HPT report

- Reliability score: 99.23% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x