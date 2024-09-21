# Results vs. 3.12.6

- fork: mpage
- ref: cec1c0b3fa171b6ab3ca
- machine: linux-x86_64
- commit hash: cec1c0b
- commit date: 2024-09-20
- overall geometric mean: 1.22x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 325 ms: 1.23x slower                                                 |
| docutils       | 2.64 sec                                               | 3.01 sec: 1.14x slower                                               |
| html5lib       | 63.6 ms                                                | 86.0 ms: 1.35x slower                                                |
| tornado_http   | 119 ms                                                 | 144 ms: 1.21x slower                                                 |
| Geometric mean | (ref)                                                  | 1.23x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 446 ms                                                 | 394 ms: 1.13x faster                                                 |
| async_tree_none            | 464 ms                                                 | 412 ms: 1.13x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 510 ms: 1.10x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 664 ms: 1.09x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 521 ms: 1.07x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 681 ms: 1.05x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 1.05 sec: 1.04x faster                                               |
| async_tree_io_tg           | 1.11 sec                                               | 1.09 sec: 1.02x faster                                               |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.54 sec: 1.02x slower                                               |
| asyncio_tcp                | 519 ms                                                 | 536 ms: 1.03x slower                                                 |
| async_generators           | 384 ms                                                 | 409 ms: 1.06x slower                                                 |
| coroutines                 | 23.9 ms                                                | 30.4 ms: 1.27x slower                                                |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 189 ms: 1.02x slower                                                 |
| float          | 80.8 ms                                                | 123 ms: 1.53x slower                                                 |
| nbody          | 89.3 ms                                                | 170 ms: 1.90x slower                                                 |
| Geometric mean | (ref)                                                  | 1.44x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.29 ms: 1.04x slower                                                |
| regex_dna      | 168 ms                                                 | 185 ms: 1.11x slower                                                 |
| regex_v8       | 20.6 ms                                                | 25.8 ms: 1.26x slower                                                |
| regex_compile  | 142 ms                                                 | 191 ms: 1.34x slower                                                 |
| Geometric mean | (ref)                                                  | 1.18x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle             | 14.1 us                                                | 13.5 us: 1.04x faster                                                |
| pickle_dict          | 31.8 us                                                | 30.5 us: 1.04x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 137 ms: 1.01x faster                                                 |
| pickle               | 10.9 us                                                | 11.2 us: 1.03x slower                                                |
| unpickle_list        | 4.67 us                                                | 4.85 us: 1.04x slower                                                |
| xml_etree_generate   | 85.2 ms                                                | 96.4 ms: 1.13x slower                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 111 ms: 1.15x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.9 ms: 1.15x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 76.7 ms: 1.30x slower                                                |
| tomli_loads          | 2.11 sec                                               | 2.78 sec: 1.32x slower                                               |
| unpickle_pure_python | 221 us                                                 | 341 us: 1.54x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 497 us: 1.62x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.14x slower                                                         |

Benchmark hidden because not significant (2): json_loads, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.39 ms: 1.03x slower                                                |
| python_startup         | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 66.5 ms: 1.33x slower                                                |
| genshi_text     | 22.8 ms                                                | 32.3 ms: 1.41x slower                                                |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                |
| django_template | 34.7 ms                                                | 51.9 ms: 1.50x slower                                                |
| Geometric mean  | (ref)                                                  | 1.41x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 446 ms                                                 | 394 ms: 1.13x faster                                                 |
| async_tree_none            | 464 ms                                                 | 412 ms: 1.13x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 510 ms: 1.10x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 664 ms: 1.09x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 521 ms: 1.07x faster                                                 |
| pathlib                    | 21.5 ms                                                | 20.4 ms: 1.06x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 681 ms: 1.05x faster                                                 |
| unpickle                   | 14.1 us                                                | 13.5 us: 1.04x faster                                                |
| pickle_dict                | 31.8 us                                                | 30.5 us: 1.04x faster                                                |
| async_tree_io              | 1.08 sec                                               | 1.05 sec: 1.04x faster                                               |
| gc_traversal               | 3.46 ms                                                | 3.38 ms: 1.02x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 1.09 sec: 1.02x faster                                               |
| json                       | 5.02 ms                                                | 4.95 ms: 1.02x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 137 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                 |
| deepcopy                   | 352 us                                                 | 355 us: 1.01x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.54 sec: 1.02x slower                                               |
| pidigits                   | 184 ms                                                 | 189 ms: 1.02x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 11.1 ms: 1.03x slower                                                |
| pickle                     | 10.9 us                                                | 11.2 us: 1.03x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 7.39 ms: 1.03x slower                                                |
| asyncio_tcp                | 519 ms                                                 | 536 ms: 1.03x slower                                                 |
| unpickle_list              | 4.67 us                                                | 4.85 us: 1.04x slower                                                |
| regex_effbot               | 3.17 ms                                                | 3.29 ms: 1.04x slower                                                |
| deepcopy_memo              | 40.3 us                                                | 42.3 us: 1.05x slower                                                |
| generators                 | 32.2 ms                                                | 34.0 ms: 1.05x slower                                                |
| async_generators           | 384 ms                                                 | 409 ms: 1.06x slower                                                 |
| meteor_contest             | 104 ms                                                 | 112 ms: 1.08x slower                                                 |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.11x slower                                                 |
| python_startup             | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.12x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 96.4 ms: 1.13x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 23.3 ms: 1.13x slower                                                |
| sqlite_synth               | 2.20 us                                                | 2.50 us: 1.13x slower                                                |
| docutils                   | 2.64 sec                                               | 3.01 sec: 1.14x slower                                               |
| deepcopy_reduce            | 3.08 us                                                | 3.52 us: 1.14x slower                                                |
| sympy_sum                  | 166 ms                                                 | 190 ms: 1.14x slower                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 111 ms: 1.15x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.9 ms: 1.15x slower                                                |
| scimark_fft                | 342 ms                                                 | 392 ms: 1.15x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 92.1 ms: 1.17x slower                                                |
| sympy_str                  | 292 ms                                                 | 341 ms: 1.17x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.84 sec: 1.18x slower                                               |
| comprehensions             | 19.8 us                                                | 23.5 us: 1.18x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 90.8 ms: 1.19x slower                                                |
| bpe_tokeniser              | 4.74 sec                                               | 5.64 sec: 1.19x slower                                               |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.23 ms: 1.19x slower                                                |
| pylint                     | 319 ms                                                 | 380 ms: 1.19x slower                                                 |
| nqueens                    | 80.1 ms                                                | 95.8 ms: 1.20x slower                                                |
| sympy_expand               | 468 ms                                                 | 562 ms: 1.20x slower                                                 |
| tornado_http               | 119 ms                                                 | 144 ms: 1.21x slower                                                 |
| coverage                   | 71.4 ms                                                | 86.6 ms: 1.21x slower                                                |
| fannkuch                   | 372 ms                                                 | 454 ms: 1.22x slower                                                 |
| telco                      | 6.53 ms                                                | 7.97 ms: 1.22x slower                                                |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.22x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                                |
| 2to3                       | 264 ms                                                 | 325 ms: 1.23x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 25.8 ms: 1.26x slower                                                |
| thrift                     | 791 us                                                 | 994 us: 1.26x slower                                                 |
| coroutines                 | 23.9 ms                                                | 30.4 ms: 1.27x slower                                                |
| pycparser                  | 1.17 sec                                               | 1.50 sec: 1.28x slower                                               |
| xml_etree_process          | 59.0 ms                                                | 76.7 ms: 1.30x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.78 sec: 1.32x slower                                               |
| genshi_xml                 | 50.2 ms                                                | 66.5 ms: 1.33x slower                                                |
| regex_compile              | 142 ms                                                 | 191 ms: 1.34x slower                                                 |
| html5lib                   | 63.6 ms                                                | 86.0 ms: 1.35x slower                                                |
| genshi_text                | 22.8 ms                                                | 32.3 ms: 1.41x slower                                                |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                |
| spectral_norm              | 110 ms                                                 | 156 ms: 1.42x slower                                                 |
| pyflate                    | 448 ms                                                 | 639 ms: 1.43x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 152 ms: 1.43x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 76.7 ms: 1.44x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 2.20 sec: 1.45x slower                                               |
| richards                   | 45.9 ms                                                | 66.8 ms: 1.45x slower                                                |
| logging_format             | 7.35 us                                                | 10.7 us: 1.45x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 1.08 sec: 1.46x slower                                               |
| logging_simple             | 6.63 us                                                | 9.66 us: 1.46x slower                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 102 ms: 1.49x slower                                                 |
| django_template            | 34.7 ms                                                | 51.9 ms: 1.50x slower                                                |
| sqlglot_transpile          | 1.67 ms                                                | 2.54 ms: 1.52x slower                                                |
| float                      | 80.8 ms                                                | 123 ms: 1.53x slower                                                 |
| richards_super             | 51.9 ms                                                | 79.8 ms: 1.54x slower                                                |
| chaos                      | 62.8 ms                                                | 96.8 ms: 1.54x slower                                                |
| unpickle_pure_python       | 221 us                                                 | 341 us: 1.54x slower                                                 |
| raytrace                   | 299 ms                                                 | 463 ms: 1.55x slower                                                 |
| hexiom                     | 6.17 ms                                                | 9.61 ms: 1.56x slower                                                |
| logging_silent             | 109 ns                                                 | 171 ns: 1.57x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 2.14 ms: 1.58x slower                                                |
| pickle_pure_python         | 308 us                                                 | 497 us: 1.62x slower                                                 |
| go                         | 139 ms                                                 | 229 ms: 1.64x slower                                                 |
| scimark_sor                | 130 ms                                                 | 220 ms: 1.70x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 199 ms: 1.74x slower                                                 |
| nbody                      | 89.3 ms                                                | 170 ms: 1.90x slower                                                 |
| deltablue                  | 3.45 ms                                                | 6.95 ms: 2.02x slower                                                |
| unpack_sequence            | 52.1 ns                                                | 106 ns: 2.04x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.22x slower                                                         |

Benchmark hidden because not significant (2): json_loads, pickle_list
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.01x