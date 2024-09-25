# Results vs. 3.12.6

- fork: python
- ref: b2afe2aae487ebf89897
- machine: linux-x86_64
- commit hash: b2afe2a
- commit date: 2024-09-12
- overall geometric mean: 1.39x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 721 ms: 1.58x slower                                                  |
| docutils       | 4.00 sec                                               | 5.09 sec: 1.27x slower                                                |
| html5lib       | 88.9 ms                                                | 141 ms: 1.59x slower                                                  |
| tornado_http   | 266 ms                                                 | 369 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                  | 1.45x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.26 sec: 1.54x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 649 ms: 1.43x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 491 ms: 1.43x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.35 sec: 1.37x faster                                                |
| async_tree_memoization     | 977 ms                                                 | 750 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 906 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 915 ms: 1.18x faster                                                  |
| async_tree_none            | 741 ms                                                 | 647 ms: 1.15x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 792 ms: 1.06x slower                                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.12 sec: 1.11x slower                                                |
| async_generators           | 589 ms                                                 | 726 ms: 1.23x slower                                                  |
| asyncio_tcp                | 923 ms                                                 | 1.19 sec: 1.29x slower                                                |
| coroutines                 | 29.5 ms                                                | 44.1 ms: 1.49x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 202 ms: 1.64x slower                                                  |
| nbody          | 119 ms                                                 | 286 ms: 2.40x slower                                                  |
| Geometric mean | (ref)                                                  | 1.60x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 278 ms                                                 | 290 ms: 1.04x slower                                                  |
| regex_v8       | 32.5 ms                                                | 36.2 ms: 1.12x slower                                                 |
| regex_compile  | 187 ms                                                 | 301 ms: 1.61x slower                                                  |
| Geometric mean | (ref)                                                  | 1.16x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 46.1 us: 1.14x faster                                                 |
| pickle               | 16.4 us                                                | 14.5 us: 1.13x faster                                                 |
| xml_etree_parse      | 241 ms                                                 | 229 ms: 1.05x faster                                                  |
| json_loads           | 37.9 us                                                | 42.8 us: 1.13x slower                                                 |
| unpickle_list        | 6.83 us                                                | 7.76 us: 1.14x slower                                                 |
| unpickle             | 21.2 us                                                | 24.2 us: 1.14x slower                                                 |
| json_dumps           | 14.3 ms                                                | 18.0 ms: 1.26x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 165 ms: 1.30x slower                                                  |
| tomli_loads          | 2.88 sec                                               | 4.26 sec: 1.48x slower                                                |
| xml_etree_process    | 83.7 ms                                                | 128 ms: 1.53x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 835 us: 1.92x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 581 us: 1.94x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.21x slower                                                          |

Benchmark hidden because not significant (2): pickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 23.8 ms: 1.35x slower                                                 |
| python_startup         | 23.7 ms                                                | 35.1 ms: 1.48x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.42x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 114 ms: 1.69x slower                                                  |
| django_template | 44.9 ms                                                | 82.9 ms: 1.84x slower                                                 |
| mako            | 15.7 ms                                                | 30.3 ms: 1.93x slower                                                 |
| genshi_text     | 30.2 ms                                                | 61.0 ms: 2.02x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.87x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.26 sec: 1.54x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 649 ms: 1.43x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 491 ms: 1.43x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.35 sec: 1.37x faster                                                |
| async_tree_memoization     | 977 ms                                                 | 750 ms: 1.30x faster                                                  |
| gc_traversal               | 5.86 ms                                                | 4.51 ms: 1.30x faster                                                 |
| bench_mp_pool              | 20.7 ms                                                | 16.5 ms: 1.26x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 906 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 915 ms: 1.18x faster                                                  |
| async_tree_none            | 741 ms                                                 | 647 ms: 1.15x faster                                                  |
| pickle_dict                | 52.7 us                                                | 46.1 us: 1.14x faster                                                 |
| pickle                     | 16.4 us                                                | 14.5 us: 1.13x faster                                                 |
| create_gc_cycles           | 1.94 ms                                                | 1.83 ms: 1.06x faster                                                 |
| xml_etree_parse            | 241 ms                                                 | 229 ms: 1.05x faster                                                  |
| regex_dna                  | 278 ms                                                 | 290 ms: 1.04x slower                                                  |
| asyncio_websockets         | 748 ms                                                 | 792 ms: 1.06x slower                                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.12 sec: 1.11x slower                                                |
| regex_v8                   | 32.5 ms                                                | 36.2 ms: 1.12x slower                                                 |
| json_loads                 | 37.9 us                                                | 42.8 us: 1.13x slower                                                 |
| unpickle_list              | 6.83 us                                                | 7.76 us: 1.14x slower                                                 |
| unpickle                   | 21.2 us                                                | 24.2 us: 1.14x slower                                                 |
| sqlite_synth               | 3.87 us                                                | 4.43 us: 1.14x slower                                                 |
| pathlib                    | 31.6 ms                                                | 36.3 ms: 1.15x slower                                                 |
| json                       | 6.85 ms                                                | 8.13 ms: 1.19x slower                                                 |
| bench_thread_pool          | 3.48 ms                                                | 4.27 ms: 1.23x slower                                                 |
| async_generators           | 589 ms                                                 | 726 ms: 1.23x slower                                                  |
| dulwich_log                | 100 ms                                                 | 125 ms: 1.25x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 18.0 ms: 1.26x slower                                                 |
| deepcopy                   | 468 us                                                 | 595 us: 1.27x slower                                                  |
| scimark_fft                | 500 ms                                                 | 636 ms: 1.27x slower                                                  |
| docutils                   | 4.00 sec                                               | 5.09 sec: 1.27x slower                                                |
| asyncio_tcp                | 923 ms                                                 | 1.19 sec: 1.29x slower                                                |
| xml_etree_generate         | 127 ms                                                 | 165 ms: 1.30x slower                                                  |
| mdp                        | 3.97 sec                                               | 5.18 sec: 1.31x slower                                                |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.99 ms: 1.34x slower                                                 |
| pylint                     | 465 ms                                                 | 627 ms: 1.35x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 23.8 ms: 1.35x slower                                                 |
| pycparser                  | 1.79 sec                                               | 2.43 sec: 1.36x slower                                                |
| deepcopy_memo              | 52.4 us                                                | 71.2 us: 1.36x slower                                                 |
| meteor_contest             | 146 ms                                                 | 199 ms: 1.36x slower                                                  |
| generators                 | 41.1 ms                                                | 56.1 ms: 1.36x slower                                                 |
| tornado_http               | 266 ms                                                 | 369 ms: 1.39x slower                                                  |
| deepcopy_reduce            | 4.04 us                                                | 5.61 us: 1.39x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 153 ms: 1.43x slower                                                  |
| pyflate                    | 727 ms                                                 | 1.06 sec: 1.45x slower                                                |
| fannkuch                   | 540 ms                                                 | 786 ms: 1.45x slower                                                  |
| tomli_loads                | 2.88 sec                                               | 4.26 sec: 1.48x slower                                                |
| python_startup             | 23.7 ms                                                | 35.1 ms: 1.48x slower                                                 |
| typing_runtime_protocols   | 224 us                                                 | 334 us: 1.49x slower                                                  |
| comprehensions             | 27.1 us                                                | 40.4 us: 1.49x slower                                                 |
| coroutines                 | 29.5 ms                                                | 44.1 ms: 1.49x slower                                                 |
| sympy_integrate            | 29.8 ms                                                | 44.8 ms: 1.51x slower                                                 |
| nqueens                    | 117 ms                                                 | 177 ms: 1.51x slower                                                  |
| telco                      | 9.59 ms                                                | 14.6 ms: 1.52x slower                                                 |
| thrift                     | 1.06 ms                                                | 1.61 ms: 1.52x slower                                                 |
| xml_etree_process          | 83.7 ms                                                | 128 ms: 1.53x slower                                                  |
| sqlglot_normalize          | 157 ms                                                 | 245 ms: 1.56x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 10.4 sec: 1.58x slower                                                |
| 2to3                       | 456 ms                                                 | 721 ms: 1.58x slower                                                  |
| html5lib                   | 88.9 ms                                                | 141 ms: 1.59x slower                                                  |
| regex_compile              | 187 ms                                                 | 301 ms: 1.61x slower                                                  |
| coverage                   | 95.4 ms                                                | 154 ms: 1.62x slower                                                  |
| float                      | 123 ms                                                 | 202 ms: 1.64x slower                                                  |
| spectral_norm              | 156 ms                                                 | 260 ms: 1.67x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 114 ms: 1.69x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 164 ms: 1.70x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.70 sec: 1.76x slower                                                |
| logging_simple             | 9.45 us                                                | 16.7 us: 1.76x slower                                                 |
| sqlglot_optimize           | 76.0 ms                                                | 134 ms: 1.76x slower                                                  |
| richards                   | 60.3 ms                                                | 107 ms: 1.78x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 3.58 sec: 1.81x slower                                                |
| django_template            | 44.9 ms                                                | 82.9 ms: 1.84x slower                                                 |
| logging_format             | 9.59 us                                                | 17.9 us: 1.86x slower                                                 |
| sympy_str                  | 385 ms                                                 | 721 ms: 1.87x slower                                                  |
| raytrace                   | 408 ms                                                 | 764 ms: 1.87x slower                                                  |
| richards_super             | 72.8 ms                                                | 137 ms: 1.88x slower                                                  |
| logging_silent             | 139 ns                                                 | 262 ns: 1.88x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 835 us: 1.92x slower                                                  |
| mako                       | 15.7 ms                                                | 30.3 ms: 1.93x slower                                                 |
| unpickle_pure_python       | 300 us                                                 | 581 us: 1.94x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 302 ms: 1.98x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 4.66 ms: 1.99x slower                                                 |
| genshi_text                | 30.2 ms                                                | 61.0 ms: 2.02x slower                                                 |
| chaos                      | 84.9 ms                                                | 172 ms: 2.03x slower                                                  |
| hexiom                     | 8.27 ms                                                | 16.9 ms: 2.04x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 460 ms: 2.07x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.75 ms: 2.10x slower                                                 |
| go                         | 172 ms                                                 | 363 ms: 2.11x slower                                                  |
| scimark_sor                | 167 ms                                                 | 367 ms: 2.21x slower                                                  |
| sympy_expand               | 582 ms                                                 | 1.31 sec: 2.26x slower                                                |
| nbody                      | 119 ms                                                 | 286 ms: 2.40x slower                                                  |
| deltablue                  | 4.27 ms                                                | 11.4 ms: 2.66x slower                                                 |
| unpack_sequence            | 60.2 ns                                                | 220 ns: 3.65x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.39x slower                                                          |

Benchmark hidden because not significant (4): regex_effbot, pickle_list, xml_etree_iterparse, pidigits
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.15x