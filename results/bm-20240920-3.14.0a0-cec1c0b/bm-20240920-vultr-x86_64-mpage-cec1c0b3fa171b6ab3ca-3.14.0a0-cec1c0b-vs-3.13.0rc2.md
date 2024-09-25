# Results vs. 3.13.0rc2

- fork: mpage
- ref: cec1c0b3fa171b6ab3ca
- machine: linux-x86_64
- commit hash: cec1c0b
- commit date: 2024-09-20
- overall geometric mean: 1.26x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 325 ms: 1.25x slower                                                 |
| docutils       | 2.62 sec                                                     | 3.01 sec: 1.15x slower                                               |
| html5lib       | 67.0 ms                                                      | 86.0 ms: 1.28x slower                                                |
| tornado_http   | 114 ms                                                       | 144 ms: 1.27x slower                                                 |
| Geometric mean | (ref)                                                        | 1.24x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.54 sec: 1.02x slower                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 681 ms: 1.02x slower                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 664 ms: 1.04x slower                                                 |
| asyncio_tcp                | 505 ms                                                       | 536 ms: 1.06x slower                                                 |
| async_generators           | 377 ms                                                       | 409 ms: 1.08x slower                                                 |
| async_tree_memoization     | 461 ms                                                       | 521 ms: 1.13x slower                                                 |
| async_tree_none            | 354 ms                                                       | 412 ms: 1.17x slower                                                 |
| async_tree_none_tg         | 336 ms                                                       | 394 ms: 1.17x slower                                                 |
| async_tree_io_tg           | 913 ms                                                       | 1.09 sec: 1.19x slower                                               |
| async_tree_io              | 876 ms                                                       | 1.05 sec: 1.19x slower                                               |
| async_tree_memoization_tg  | 414 ms                                                       | 510 ms: 1.23x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 30.4 ms: 1.29x slower                                                |
| Geometric mean             | (ref)                                                        | 1.12x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 189 ms: 1.15x faster                                                 |
| float          | 77.5 ms                                                      | 123 ms: 1.59x slower                                                 |
| nbody          | 85.1 ms                                                      | 170 ms: 2.00x slower                                                 |
| Geometric mean | (ref)                                                        | 1.41x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                       | 185 ms: 1.03x slower                                                 |
| regex_effbot   | 3.08 ms                                                      | 3.29 ms: 1.07x slower                                                |
| regex_v8       | 22.7 ms                                                      | 25.8 ms: 1.14x slower                                                |
| regex_compile  | 132 ms                                                       | 191 ms: 1.44x slower                                                 |
| Geometric mean | (ref)                                                        | 1.16x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.5 us: 1.07x faster                                                |
| unpickle             | 14.3 us                                                      | 13.5 us: 1.06x faster                                                |
| pickle_list          | 4.93 us                                                      | 4.76 us: 1.03x faster                                                |
| json_loads           | 27.0 us                                                      | 26.4 us: 1.02x faster                                                |
| pickle               | 11.3 us                                                      | 11.2 us: 1.01x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 137 ms: 1.01x slower                                                 |
| unpickle_list        | 4.71 us                                                      | 4.85 us: 1.03x slower                                                |
| json_dumps           | 10.5 ms                                                      | 11.9 ms: 1.13x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 96.4 ms: 1.13x slower                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 111 ms: 1.17x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 76.7 ms: 1.29x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 2.78 sec: 1.39x slower                                               |
| unpickle_pure_python | 210 us                                                       | 341 us: 1.62x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 497 us: 1.69x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.14x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup | 11.0 ms                                                      | 11.0 ms: 1.00x slower                                                |
| Geometric mean | (ref)                                                        | 1.00x slower                                                         |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 66.5 ms: 1.36x slower                                                |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                |
| genshi_text     | 21.5 ms                                                      | 32.3 ms: 1.50x slower                                                |
| django_template | 34.1 ms                                                      | 51.9 ms: 1.52x slower                                                |
| Geometric mean  | (ref)                                                        | 1.44x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240920-vultr-x86_64-mpage-cec1c0b3fa171b6ab3ca-3.14.0a0-cec1c0b |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 189 ms: 1.15x faster                                                 |
| pickle_dict                | 32.5 us                                                      | 30.5 us: 1.07x faster                                                |
| unpickle                   | 14.3 us                                                      | 13.5 us: 1.06x faster                                                |
| pickle_list                | 4.93 us                                                      | 4.76 us: 1.03x faster                                                |
| json_loads                 | 27.0 us                                                      | 26.4 us: 1.02x faster                                                |
| pickle                     | 11.3 us                                                      | 11.2 us: 1.01x faster                                                |
| python_startup             | 11.0 ms                                                      | 11.0 ms: 1.00x slower                                                |
| bench_mp_pool              | 11.0 ms                                                      | 11.1 ms: 1.01x slower                                                |
| xml_etree_parse            | 136 ms                                                       | 137 ms: 1.01x slower                                                 |
| telco                      | 7.82 ms                                                      | 7.97 ms: 1.02x slower                                                |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.54 sec: 1.02x slower                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 681 ms: 1.02x slower                                                 |
| regex_dna                  | 180 ms                                                       | 185 ms: 1.03x slower                                                 |
| unpickle_list              | 4.71 us                                                      | 4.85 us: 1.03x slower                                                |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 664 ms: 1.04x slower                                                 |
| coverage                   | 83.0 ms                                                      | 86.6 ms: 1.04x slower                                                |
| asyncio_tcp                | 505 ms                                                       | 536 ms: 1.06x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 20.4 ms: 1.06x slower                                                |
| regex_effbot               | 3.08 ms                                                      | 3.29 ms: 1.07x slower                                                |
| gc_traversal               | 3.14 ms                                                      | 3.38 ms: 1.08x slower                                                |
| deepcopy_memo              | 39.1 us                                                      | 42.3 us: 1.08x slower                                                |
| async_generators           | 377 ms                                                       | 409 ms: 1.08x slower                                                 |
| meteor_contest             | 102 ms                                                       | 112 ms: 1.10x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.23 ms: 1.11x slower                                                |
| scimark_fft                | 349 ms                                                       | 392 ms: 1.12x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 11.9 ms: 1.13x slower                                                |
| xml_etree_generate         | 85.4 ms                                                      | 96.4 ms: 1.13x slower                                                |
| async_tree_memoization     | 461 ms                                                       | 521 ms: 1.13x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.52 us: 1.13x slower                                                |
| sqlite_synth               | 2.21 us                                                      | 2.50 us: 1.13x slower                                                |
| regex_v8                   | 22.7 ms                                                      | 25.8 ms: 1.14x slower                                                |
| bench_thread_pool          | 919 us                                                       | 1.05 ms: 1.14x slower                                                |
| docutils                   | 2.62 sec                                                     | 3.01 sec: 1.15x slower                                               |
| async_tree_none            | 354 ms                                                       | 412 ms: 1.17x slower                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 111 ms: 1.17x slower                                                 |
| async_tree_none_tg         | 336 ms                                                       | 394 ms: 1.17x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 23.3 ms: 1.17x slower                                                |
| generators                 | 28.8 ms                                                      | 34.0 ms: 1.18x slower                                                |
| async_tree_io_tg           | 913 ms                                                       | 1.09 sec: 1.19x slower                                               |
| async_tree_io              | 876 ms                                                       | 1.05 sec: 1.19x slower                                               |
| pylint                     | 317 ms                                                       | 380 ms: 1.20x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.84 sec: 1.21x slower                                               |
| nqueens                    | 78.6 ms                                                      | 95.8 ms: 1.22x slower                                                |
| sympy_sum                  | 156 ms                                                       | 190 ms: 1.22x slower                                                 |
| fannkuch                   | 370 ms                                                       | 454 ms: 1.23x slower                                                 |
| sympy_expand               | 457 ms                                                       | 562 ms: 1.23x slower                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 510 ms: 1.23x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 92.1 ms: 1.23x slower                                                |
| sympy_str                  | 275 ms                                                       | 341 ms: 1.24x slower                                                 |
| 2to3                       | 260 ms                                                       | 325 ms: 1.25x slower                                                 |
| tornado_http               | 114 ms                                                       | 144 ms: 1.27x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 5.64 sec: 1.27x slower                                               |
| thrift                     | 778 us                                                       | 994 us: 1.28x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 86.0 ms: 1.28x slower                                                |
| typing_runtime_protocols   | 155 us                                                       | 200 us: 1.29x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 30.4 ms: 1.29x slower                                                |
| xml_etree_process          | 59.3 ms                                                      | 76.7 ms: 1.29x slower                                                |
| crypto_pyaes               | 67.9 ms                                                      | 90.8 ms: 1.34x slower                                                |
| pycparser                  | 1.12 sec                                                     | 1.50 sec: 1.34x slower                                               |
| genshi_xml                 | 48.8 ms                                                      | 66.5 ms: 1.36x slower                                                |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                |
| tomli_loads                | 2.01 sec                                                     | 2.78 sec: 1.39x slower                                               |
| spectral_norm              | 111 ms                                                       | 156 ms: 1.41x slower                                                 |
| pyflate                    | 449 ms                                                       | 639 ms: 1.42x slower                                                 |
| comprehensions             | 16.5 us                                                      | 23.5 us: 1.43x slower                                                |
| sqlglot_normalize          | 106 ms                                                       | 152 ms: 1.44x slower                                                 |
| regex_compile              | 132 ms                                                       | 191 ms: 1.44x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 76.7 ms: 1.45x slower                                                |
| pprint_safe_repr           | 738 ms                                                       | 1.08 sec: 1.47x slower                                               |
| pprint_pformat             | 1.50 sec                                                     | 2.20 sec: 1.47x slower                                               |
| richards                   | 45.2 ms                                                      | 66.8 ms: 1.48x slower                                                |
| genshi_text                | 21.5 ms                                                      | 32.3 ms: 1.50x slower                                                |
| django_template            | 34.1 ms                                                      | 51.9 ms: 1.52x slower                                                |
| richards_super             | 51.6 ms                                                      | 79.8 ms: 1.55x slower                                                |
| scimark_monte_carlo        | 65.4 ms                                                      | 102 ms: 1.56x slower                                                 |
| logging_format             | 6.84 us                                                      | 10.7 us: 1.56x slower                                                |
| logging_simple             | 6.16 us                                                      | 9.66 us: 1.57x slower                                                |
| float                      | 77.5 ms                                                      | 123 ms: 1.59x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 9.61 ms: 1.60x slower                                                |
| unpickle_pure_python       | 210 us                                                       | 341 us: 1.62x slower                                                 |
| go                         | 141 ms                                                       | 229 ms: 1.62x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 2.54 ms: 1.63x slower                                                |
| scimark_sor                | 134 ms                                                       | 220 ms: 1.64x slower                                                 |
| logging_silent             | 103 ns                                                       | 171 ns: 1.67x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 497 us: 1.69x slower                                                 |
| chaos                      | 57.3 ms                                                      | 96.8 ms: 1.69x slower                                                |
| sqlglot_parse              | 1.25 ms                                                      | 2.14 ms: 1.72x slower                                                |
| scimark_lu                 | 113 ms                                                       | 199 ms: 1.77x slower                                                 |
| raytrace                   | 253 ms                                                       | 463 ms: 1.83x slower                                                 |
| nbody                      | 85.1 ms                                                      | 170 ms: 2.00x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 6.95 ms: 2.22x slower                                                |
| unpack_sequence            | 44.8 ns                                                      | 106 ns: 2.37x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.26x slower                                                         |

Benchmark hidden because not significant (5): deepcopy, python_startup_no_site, asyncio_websockets, create_gc_cycles, json
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 0.99x