# Results vs. 3.12.6

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.38x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 646 ms: 1.41x slower                                                 |
| docutils       | 4.00 sec                                               | 5.06 sec: 1.27x slower                                               |
| html5lib       | 88.9 ms                                                | 140 ms: 1.58x slower                                                 |
| tornado_http   | 266 ms                                                 | 367 ms: 1.38x slower                                                 |
| Geometric mean | (ref)                                                  | 1.41x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.15 sec: 1.69x faster                                               |
| async_tree_io              | 1.85 sec                                               | 1.25 sec: 1.48x faster                                               |
| async_tree_none_tg         | 704 ms                                                 | 491 ms: 1.43x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 666 ms: 1.40x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 824 ms: 1.33x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 751 ms: 1.30x faster                                                 |
| async_tree_none            | 741 ms                                                 | 585 ms: 1.27x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 933 ms: 1.16x faster                                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.36 sec: 1.20x slower                                               |
| asyncio_tcp                | 923 ms                                                 | 1.12 sec: 1.21x slower                                               |
| async_generators           | 589 ms                                                 | 753 ms: 1.28x slower                                                 |
| coroutines                 | 29.5 ms                                                | 42.1 ms: 1.43x slower                                                |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 123 ms                                                 | 196 ms: 1.59x slower                                                 |
| nbody          | 119 ms                                                 | 284 ms: 2.38x slower                                                 |
| Geometric mean | (ref)                                                  | 1.54x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.82 ms: 1.06x faster                                                |
| regex_dna      | 278 ms                                                 | 301 ms: 1.08x slower                                                 |
| regex_v8       | 32.5 ms                                                | 39.2 ms: 1.21x slower                                                |
| regex_compile  | 187 ms                                                 | 295 ms: 1.58x slower                                                 |
| Geometric mean | (ref)                                                  | 1.18x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 43.9 us: 1.20x faster                                                |
| pickle               | 16.4 us                                                | 14.1 us: 1.16x faster                                                |
| xml_etree_iterparse  | 169 ms                                                 | 179 ms: 1.06x slower                                                 |
| unpickle_list        | 6.83 us                                                | 7.94 us: 1.16x slower                                                |
| json_loads           | 37.9 us                                                | 45.4 us: 1.20x slower                                                |
| json_dumps           | 14.3 ms                                                | 17.7 ms: 1.23x slower                                                |
| xml_etree_generate   | 127 ms                                                 | 164 ms: 1.29x slower                                                 |
| tomli_loads          | 2.88 sec                                               | 4.20 sec: 1.46x slower                                               |
| xml_etree_process    | 83.7 ms                                                | 135 ms: 1.61x slower                                                 |
| pickle_pure_python   | 436 us                                                 | 778 us: 1.79x slower                                                 |
| unpickle_pure_python | 300 us                                                 | 567 us: 1.89x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.20x slower                                                         |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.7 ms: 1.18x slower                                                |
| python_startup         | 23.7 ms                                                | 29.3 ms: 1.24x slower                                                |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 77.1 ms: 1.71x slower                                                |
| genshi_xml      | 67.6 ms                                                | 118 ms: 1.74x slower                                                 |
| genshi_text     | 30.2 ms                                                | 54.2 ms: 1.79x slower                                                |
| mako            | 15.7 ms                                                | 32.1 ms: 2.04x slower                                                |
| Geometric mean  | (ref)                                                  | 1.82x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.15 sec: 1.69x faster                                               |
| async_tree_io              | 1.85 sec                                               | 1.25 sec: 1.48x faster                                               |
| async_tree_none_tg         | 704 ms                                                 | 491 ms: 1.43x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 666 ms: 1.40x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 824 ms: 1.33x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 751 ms: 1.30x faster                                                 |
| async_tree_none            | 741 ms                                                 | 585 ms: 1.27x faster                                                 |
| gc_traversal               | 5.86 ms                                                | 4.63 ms: 1.27x faster                                                |
| bench_mp_pool              | 20.7 ms                                                | 16.8 ms: 1.24x faster                                                |
| pickle_dict                | 52.7 us                                                | 43.9 us: 1.20x faster                                                |
| pickle                     | 16.4 us                                                | 14.1 us: 1.16x faster                                                |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 933 ms: 1.16x faster                                                 |
| regex_effbot               | 5.13 ms                                                | 4.82 ms: 1.06x faster                                                |
| xml_etree_iterparse        | 169 ms                                                 | 179 ms: 1.06x slower                                                 |
| regex_dna                  | 278 ms                                                 | 301 ms: 1.08x slower                                                 |
| pathlib                    | 31.6 ms                                                | 35.6 ms: 1.13x slower                                                |
| sqlite_synth               | 3.87 us                                                | 4.44 us: 1.15x slower                                                |
| unpickle_list              | 6.83 us                                                | 7.94 us: 1.16x slower                                                |
| python_startup_no_site     | 17.6 ms                                                | 20.7 ms: 1.18x slower                                                |
| deepcopy                   | 468 us                                                 | 556 us: 1.19x slower                                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.36 sec: 1.20x slower                                               |
| json_loads                 | 37.9 us                                                | 45.4 us: 1.20x slower                                                |
| json                       | 6.85 ms                                                | 8.22 ms: 1.20x slower                                                |
| regex_v8                   | 32.5 ms                                                | 39.2 ms: 1.21x slower                                                |
| asyncio_tcp                | 923 ms                                                 | 1.12 sec: 1.21x slower                                               |
| json_dumps                 | 14.3 ms                                                | 17.7 ms: 1.23x slower                                                |
| python_startup             | 23.7 ms                                                | 29.3 ms: 1.24x slower                                                |
| bench_thread_pool          | 3.48 ms                                                | 4.33 ms: 1.24x slower                                                |
| docutils                   | 4.00 sec                                               | 5.06 sec: 1.27x slower                                               |
| scimark_fft                | 500 ms                                                 | 635 ms: 1.27x slower                                                 |
| pylint                     | 465 ms                                                 | 590 ms: 1.27x slower                                                 |
| async_generators           | 589 ms                                                 | 753 ms: 1.28x slower                                                 |
| pycparser                  | 1.79 sec                                               | 2.29 sec: 1.28x slower                                               |
| xml_etree_generate         | 127 ms                                                 | 164 ms: 1.29x slower                                                 |
| mdp                        | 3.97 sec                                               | 5.16 sec: 1.30x slower                                               |
| meteor_contest             | 146 ms                                                 | 194 ms: 1.33x slower                                                 |
| deepcopy_memo              | 52.4 us                                                | 69.7 us: 1.33x slower                                                |
| nqueens                    | 117 ms                                                 | 161 ms: 1.38x slower                                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.23 ms: 1.38x slower                                                |
| tornado_http               | 266 ms                                                 | 367 ms: 1.38x slower                                                 |
| generators                 | 41.1 ms                                                | 57.5 ms: 1.40x slower                                                |
| comprehensions             | 27.1 us                                                | 38.3 us: 1.41x slower                                                |
| 2to3                       | 456 ms                                                 | 646 ms: 1.41x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 152 ms: 1.42x slower                                                 |
| coroutines                 | 29.5 ms                                                | 42.1 ms: 1.43x slower                                                |
| fannkuch                   | 540 ms                                                 | 776 ms: 1.44x slower                                                 |
| telco                      | 9.59 ms                                                | 13.8 ms: 1.44x slower                                                |
| deepcopy_reduce            | 4.04 us                                                | 5.84 us: 1.45x slower                                                |
| tomli_loads                | 2.88 sec                                               | 4.20 sec: 1.46x slower                                               |
| sympy_integrate            | 29.8 ms                                                | 44.3 ms: 1.49x slower                                                |
| pyflate                    | 727 ms                                                 | 1.09 sec: 1.50x slower                                               |
| coverage                   | 95.4 ms                                                | 146 ms: 1.53x slower                                                 |
| sqlglot_normalize          | 157 ms                                                 | 242 ms: 1.54x slower                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 10.3 sec: 1.56x slower                                               |
| html5lib                   | 88.9 ms                                                | 140 ms: 1.58x slower                                                 |
| regex_compile              | 187 ms                                                 | 295 ms: 1.58x slower                                                 |
| typing_runtime_protocols   | 224 us                                                 | 356 us: 1.59x slower                                                 |
| float                      | 123 ms                                                 | 196 ms: 1.59x slower                                                 |
| logging_simple             | 9.45 us                                                | 15.0 us: 1.59x slower                                                |
| xml_etree_process          | 83.7 ms                                                | 135 ms: 1.61x slower                                                 |
| spectral_norm              | 156 ms                                                 | 253 ms: 1.62x slower                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 160 ms: 1.66x slower                                                 |
| thrift                     | 1.06 ms                                                | 1.77 ms: 1.67x slower                                                |
| pprint_safe_repr           | 967 ms                                                 | 1.64 sec: 1.70x slower                                               |
| richards_super             | 72.8 ms                                                | 124 ms: 1.71x slower                                                 |
| django_template            | 44.9 ms                                                | 77.1 ms: 1.71x slower                                                |
| pprint_pformat             | 1.98 sec                                               | 3.45 sec: 1.74x slower                                               |
| genshi_xml                 | 67.6 ms                                                | 118 ms: 1.74x slower                                                 |
| sympy_str                  | 385 ms                                                 | 673 ms: 1.75x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 778 us: 1.79x slower                                                 |
| genshi_text                | 30.2 ms                                                | 54.2 ms: 1.79x slower                                                |
| richards                   | 60.3 ms                                                | 110 ms: 1.82x slower                                                 |
| logging_silent             | 139 ns                                                 | 254 ns: 1.83x slower                                                 |
| raytrace                   | 408 ms                                                 | 765 ms: 1.88x slower                                                 |
| sqlglot_optimize           | 76.0 ms                                                | 143 ms: 1.89x slower                                                 |
| unpickle_pure_python       | 300 us                                                 | 567 us: 1.89x slower                                                 |
| logging_format             | 9.59 us                                                | 18.5 us: 1.93x slower                                                |
| sqlglot_transpile          | 2.34 ms                                                | 4.62 ms: 1.98x slower                                                |
| chaos                      | 84.9 ms                                                | 169 ms: 1.99x slower                                                 |
| scimark_lu                 | 152 ms                                                 | 303 ms: 1.99x slower                                                 |
| mako                       | 15.7 ms                                                | 32.1 ms: 2.04x slower                                                |
| scimark_sor                | 167 ms                                                 | 342 ms: 2.05x slower                                                 |
| hexiom                     | 8.27 ms                                                | 17.2 ms: 2.07x slower                                                |
| sympy_sum                  | 222 ms                                                 | 465 ms: 2.10x slower                                                 |
| sympy_expand               | 582 ms                                                 | 1.26 sec: 2.17x slower                                               |
| nbody                      | 119 ms                                                 | 284 ms: 2.38x slower                                                 |
| sqlglot_parse              | 1.79 ms                                                | 4.43 ms: 2.48x slower                                                |
| go                         | 172 ms                                                 | 446 ms: 2.59x slower                                                 |
| deltablue                  | 4.27 ms                                                | 11.3 ms: 2.66x slower                                                |
| unpack_sequence            | 60.2 ns                                                | 211 ns: 3.50x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.38x slower                                                         |

Benchmark hidden because not significant (6): xml_etree_parse, pidigits, pickle_list, create_gc_cycles, asyncio_websockets, unpickle
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.15x