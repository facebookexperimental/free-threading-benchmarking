# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5a4fb7e
- commit date: 2024-09-06
- overall geometric mean: 1.46x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.33x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 442 ms                                                  | 682 ms: 1.54x slower                                  |
| docutils       | 4.01 sec                                                | 5.10 sec: 1.27x slower                                |
| html5lib       | 98.1 ms                                                 | 147 ms: 1.50x slower                                  |
| tornado_http   | 248 ms                                                  | 420 ms: 1.69x slower                                  |
| Geometric mean | (ref)                                                   | 1.50x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.46 sec                                                | 1.24 sec: 1.18x faster                                |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 885 ms: 1.04x slower                                  |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 937 ms: 1.04x slower                                  |
| async_tree_none            | 576 ms                                                  | 607 ms: 1.05x slower                                  |
| asyncio_websockets         | 772 ms                                                  | 818 ms: 1.06x slower                                  |
| async_generators           | 592 ms                                                  | 723 ms: 1.22x slower                                  |
| asyncio_tcp                | 985 ms                                                  | 1.22 sec: 1.24x slower                                |
| asyncio_tcp_ssl            | 2.79 sec                                                | 3.67 sec: 1.32x slower                                |
| coroutines                 | 29.2 ms                                                 | 42.2 ms: 1.44x slower                                 |
| Geometric mean             | (ref)                                                   | 1.09x slower                                          |

Benchmark hidden because not significant (4): async_tree_io, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 248 ms                                                  | 258 ms: 1.04x slower                                  |
| float          | 115 ms                                                  | 203 ms: 1.76x slower                                  |
| nbody          | 124 ms                                                  | 315 ms: 2.55x slower                                  |
| Geometric mean | (ref)                                                   | 1.67x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 288 ms                                                  | 299 ms: 1.04x slower                                  |
| regex_effbot   | 4.84 ms                                                 | 5.21 ms: 1.08x slower                                 |
| regex_v8       | 32.4 ms                                                 | 37.6 ms: 1.16x slower                                 |
| regex_compile  | 177 ms                                                  | 305 ms: 1.72x slower                                  |
| Geometric mean | (ref)                                                   | 1.22x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| pickle               | 15.4 us                                                 | 13.8 us: 1.11x faster                                 |
| pickle_list          | 6.82 us                                                 | 6.51 us: 1.05x faster                                 |
| unpickle             | 21.4 us                                                 | 23.1 us: 1.08x slower                                 |
| unpickle_list        | 6.67 us                                                 | 7.45 us: 1.12x slower                                 |
| json_dumps           | 14.9 ms                                                 | 18.0 ms: 1.21x slower                                 |
| json_loads           | 36.1 us                                                 | 47.7 us: 1.32x slower                                 |
| xml_etree_generate   | 129 ms                                                  | 179 ms: 1.39x slower                                  |
| tomli_loads          | 2.80 sec                                                | 4.37 sec: 1.56x slower                                |
| xml_etree_process    | 86.5 ms                                                 | 136 ms: 1.57x slower                                  |
| pickle_pure_python   | 417 us                                                  | 762 us: 1.83x slower                                  |
| unpickle_pure_python | 296 us                                                  | 563 us: 1.90x slower                                  |
| Geometric mean       | (ref)                                                   | 1.23x slower                                          |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_parse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 14.6 ms                                                 | 24.3 ms: 1.66x slower                                 |
| python_startup         | 22.0 ms                                                 | 37.1 ms: 1.68x slower                                 |
| Geometric mean         | (ref)                                                   | 1.67x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|-----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 46.9 ms                                                 | 83.6 ms: 1.78x slower                                 |
| genshi_text     | 31.7 ms                                                 | 57.6 ms: 1.81x slower                                 |
| mako            | 16.1 ms                                                 | 31.9 ms: 1.98x slower                                 |
| genshi_xml      | 68.3 ms                                                 | 141 ms: 2.06x slower                                  |
| Geometric mean  | (ref)                                                   | 1.91x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| create_gc_cycles           | 2.46 ms                                                 | 1.96 ms: 1.25x faster                                 |
| gc_traversal               | 5.91 ms                                                 | 4.74 ms: 1.25x faster                                 |
| async_tree_io_tg           | 1.46 sec                                                | 1.24 sec: 1.18x faster                                |
| pickle                     | 15.4 us                                                 | 13.8 us: 1.11x faster                                 |
| pickle_list                | 6.82 us                                                 | 6.51 us: 1.05x faster                                 |
| regex_dna                  | 288 ms                                                  | 299 ms: 1.04x slower                                  |
| pidigits                   | 248 ms                                                  | 258 ms: 1.04x slower                                  |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 885 ms: 1.04x slower                                  |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 937 ms: 1.04x slower                                  |
| async_tree_none            | 576 ms                                                  | 607 ms: 1.05x slower                                  |
| asyncio_websockets         | 772 ms                                                  | 818 ms: 1.06x slower                                  |
| regex_effbot               | 4.84 ms                                                 | 5.21 ms: 1.08x slower                                 |
| unpickle                   | 21.4 us                                                 | 23.1 us: 1.08x slower                                 |
| unpickle_list              | 6.67 us                                                 | 7.45 us: 1.12x slower                                 |
| regex_v8                   | 32.4 ms                                                 | 37.6 ms: 1.16x slower                                 |
| json_dumps                 | 14.9 ms                                                 | 18.0 ms: 1.21x slower                                 |
| async_generators           | 592 ms                                                  | 723 ms: 1.22x slower                                  |
| pathlib                    | 29.3 ms                                                 | 36.2 ms: 1.24x slower                                 |
| asyncio_tcp                | 985 ms                                                  | 1.22 sec: 1.24x slower                                |
| meteor_contest             | 157 ms                                                  | 196 ms: 1.25x slower                                  |
| docutils                   | 4.01 sec                                                | 5.10 sec: 1.27x slower                                |
| deepcopy                   | 484 us                                                  | 617 us: 1.27x slower                                  |
| telco                      | 11.4 ms                                                 | 14.9 ms: 1.30x slower                                 |
| coverage                   | 110 ms                                                  | 144 ms: 1.31x slower                                  |
| asyncio_tcp_ssl            | 2.79 sec                                                | 3.67 sec: 1.32x slower                                |
| scimark_sparse_mat_mult    | 6.98 ms                                                 | 9.21 ms: 1.32x slower                                 |
| json_loads                 | 36.1 us                                                 | 47.7 us: 1.32x slower                                 |
| mdp                        | 3.80 sec                                                | 5.07 sec: 1.34x slower                                |
| pylint                     | 472 ms                                                  | 641 ms: 1.36x slower                                  |
| deepcopy_reduce            | 4.27 us                                                 | 5.81 us: 1.36x slower                                 |
| deepcopy_memo              | 51.7 us                                                 | 71.0 us: 1.37x slower                                 |
| json                       | 6.55 ms                                                 | 9.01 ms: 1.38x slower                                 |
| scimark_fft                | 477 ms                                                  | 659 ms: 1.38x slower                                  |
| xml_etree_generate         | 129 ms                                                  | 179 ms: 1.39x slower                                  |
| dulwich_log                | 100.0 ms                                                | 143 ms: 1.43x slower                                  |
| generators                 | 39.2 ms                                                 | 56.6 ms: 1.44x slower                                 |
| coroutines                 | 29.2 ms                                                 | 42.2 ms: 1.44x slower                                 |
| pycparser                  | 1.57 sec                                                | 2.29 sec: 1.46x slower                                |
| fannkuch                   | 543 ms                                                  | 807 ms: 1.49x slower                                  |
| html5lib                   | 98.1 ms                                                 | 147 ms: 1.50x slower                                  |
| thrift                     | 1.11 ms                                                 | 1.68 ms: 1.51x slower                                 |
| 2to3                       | 442 ms                                                  | 682 ms: 1.54x slower                                  |
| tomli_loads                | 2.80 sec                                                | 4.37 sec: 1.56x slower                                |
| xml_etree_process          | 86.5 ms                                                 | 136 ms: 1.57x slower                                  |
| nqueens                    | 108 ms                                                  | 170 ms: 1.57x slower                                  |
| crypto_pyaes               | 99.8 ms                                                 | 158 ms: 1.58x slower                                  |
| spectral_norm              | 159 ms                                                  | 253 ms: 1.59x slower                                  |
| richards                   | 65.8 ms                                                 | 107 ms: 1.62x slower                                  |
| sqlglot_optimize           | 76.2 ms                                                 | 125 ms: 1.64x slower                                  |
| richards_super             | 76.3 ms                                                 | 126 ms: 1.65x slower                                  |
| typing_runtime_protocols   | 216 us                                                  | 357 us: 1.65x slower                                  |
| python_startup_no_site     | 14.6 ms                                                 | 24.3 ms: 1.66x slower                                 |
| sympy_integrate            | 29.7 ms                                                 | 49.3 ms: 1.66x slower                                 |
| pyflate                    | 661 ms                                                  | 1.11 sec: 1.68x slower                                |
| python_startup             | 22.0 ms                                                 | 37.1 ms: 1.68x slower                                 |
| tornado_http               | 248 ms                                                  | 420 ms: 1.69x slower                                  |
| sqlglot_normalize          | 146 ms                                                  | 248 ms: 1.70x slower                                  |
| regex_compile              | 177 ms                                                  | 305 ms: 1.72x slower                                  |
| bpe_tokeniser              | 6.25 sec                                                | 10.8 sec: 1.72x slower                                |
| pprint_safe_repr           | 959 ms                                                  | 1.66 sec: 1.73x slower                                |
| bench_thread_pool          | 3.06 ms                                                 | 5.33 ms: 1.74x slower                                 |
| float                      | 115 ms                                                  | 203 ms: 1.76x slower                                  |
| pprint_pformat             | 2.00 sec                                                | 3.55 sec: 1.78x slower                                |
| django_template            | 46.9 ms                                                 | 83.6 ms: 1.78x slower                                 |
| logging_simple             | 8.98 us                                                 | 16.0 us: 1.78x slower                                 |
| genshi_text                | 31.7 ms                                                 | 57.6 ms: 1.81x slower                                 |
| pickle_pure_python         | 417 us                                                  | 762 us: 1.83x slower                                  |
| logging_format             | 9.48 us                                                 | 17.5 us: 1.84x slower                                 |
| go                         | 195 ms                                                  | 370 ms: 1.89x slower                                  |
| scimark_monte_carlo        | 89.9 ms                                                 | 171 ms: 1.90x slower                                  |
| unpickle_pure_python       | 296 us                                                  | 563 us: 1.90x slower                                  |
| chaos                      | 84.7 ms                                                 | 163 ms: 1.92x slower                                  |
| sympy_str                  | 367 ms                                                  | 708 ms: 1.93x slower                                  |
| comprehensions             | 20.9 us                                                 | 41.3 us: 1.97x slower                                 |
| mako                       | 16.1 ms                                                 | 31.9 ms: 1.98x slower                                 |
| logging_silent             | 130 ns                                                  | 266 ns: 2.05x slower                                  |
| hexiom                     | 8.35 ms                                                 | 17.1 ms: 2.05x slower                                 |
| sqlglot_transpile          | 2.30 ms                                                 | 4.73 ms: 2.06x slower                                 |
| genshi_xml                 | 68.3 ms                                                 | 141 ms: 2.06x slower                                  |
| sqlglot_parse              | 1.80 ms                                                 | 3.76 ms: 2.09x slower                                 |
| sympy_expand               | 631 ms                                                  | 1.32 sec: 2.09x slower                                |
| scimark_sor                | 172 ms                                                  | 360 ms: 2.09x slower                                  |
| scimark_lu                 | 154 ms                                                  | 328 ms: 2.13x slower                                  |
| sympy_sum                  | 213 ms                                                  | 472 ms: 2.21x slower                                  |
| raytrace                   | 350 ms                                                  | 798 ms: 2.28x slower                                  |
| nbody                      | 124 ms                                                  | 315 ms: 2.55x slower                                  |
| deltablue                  | 4.56 ms                                                 | 12.2 ms: 2.66x slower                                 |
| unpack_sequence            | 73.9 ns                                                 | 207 ns: 2.80x slower                                  |
| Geometric mean             | (ref)                                                   | 1.46x slower                                          |

Benchmark hidden because not significant (9): xml_etree_iterparse, async_tree_io, xml_etree_parse, pickle_dict, async_tree_memoization_tg, bench_mp_pool, async_tree_memoization, async_tree_none_tg, sqlite_synth
Ignored benchmarks (5) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.40x
- 95% likely to have a slowdown of 1.37x
- 99% likely to have a slowdown of 1.33x

# Memory
- memory change: 1.14x