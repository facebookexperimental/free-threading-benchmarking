# Results vs. 3.13.0rc1+

- fork: mpage
- ref: f4d1deda87c7c7bcf4b1
- machine: linux-x86_64
- commit hash: f4d1ded
- commit date: 2024-09-04
- overall geometric mean: 1.25x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 442 ms                                                  | 546 ms: 1.24x slower                                                 |
| docutils       | 4.01 sec                                                | 4.52 sec: 1.13x slower                                               |
| html5lib       | 98.1 ms                                                 | 130 ms: 1.32x slower                                                 |
| tornado_http   | 248 ms                                                  | 334 ms: 1.35x slower                                                 |
| Geometric mean | (ref)                                                   | 1.26x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.46 sec                                                | 1.56 sec: 1.07x slower                                               |
| async_generators           | 592 ms                                                  | 637 ms: 1.08x slower                                                 |
| async_tree_memoization     | 745 ms                                                  | 809 ms: 1.09x slower                                                 |
| async_tree_none            | 576 ms                                                  | 636 ms: 1.10x slower                                                 |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 1.01 sec: 1.12x slower                                               |
| async_tree_io              | 1.38 sec                                                | 1.55 sec: 1.13x slower                                               |
| async_tree_memoization_tg  | 672 ms                                                  | 760 ms: 1.13x slower                                                 |
| async_tree_none_tg         | 521 ms                                                  | 609 ms: 1.17x slower                                                 |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 1.01 sec: 1.19x slower                                               |
| coroutines                 | 29.2 ms                                                 | 38.7 ms: 1.33x slower                                                |
| Geometric mean             | (ref)                                                   | 1.10x slower                                                         |

Benchmark hidden because not significant (3): asyncio_websockets, asyncio_tcp, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 115 ms                                                  | 171 ms: 1.49x slower                                                 |
| nbody          | 124 ms                                                  | 226 ms: 1.82x slower                                                 |
| Geometric mean | (ref)                                                   | 1.40x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 288 ms                                                  | 304 ms: 1.06x slower                                                 |
| regex_v8       | 32.4 ms                                                 | 38.6 ms: 1.19x slower                                                |
| regex_compile  | 177 ms                                                  | 253 ms: 1.42x slower                                                 |
| Geometric mean | (ref)                                                   | 1.16x slower                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle             | 21.4 us                                                 | 19.4 us: 1.10x faster                                                |
| xml_etree_parse      | 236 ms                                                  | 223 ms: 1.06x faster                                                 |
| xml_etree_generate   | 129 ms                                                  | 142 ms: 1.10x slower                                                 |
| xml_etree_iterparse  | 176 ms                                                  | 196 ms: 1.11x slower                                                 |
| json_loads           | 36.1 us                                                 | 40.3 us: 1.12x slower                                                |
| json_dumps           | 14.9 ms                                                 | 16.8 ms: 1.13x slower                                                |
| unpickle_list        | 6.67 us                                                 | 7.52 us: 1.13x slower                                                |
| xml_etree_process    | 86.5 ms                                                 | 110 ms: 1.27x slower                                                 |
| tomli_loads          | 2.80 sec                                                | 3.74 sec: 1.33x slower                                               |
| unpickle_pure_python | 296 us                                                  | 461 us: 1.56x slower                                                 |
| pickle_pure_python   | 417 us                                                  | 673 us: 1.61x slower                                                 |
| Geometric mean       | (ref)                                                   | 1.13x slower                                                         |

Benchmark hidden because not significant (3): pickle_dict, pickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|------------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 23.5 ms: 1.07x slower                                                |
| python_startup_no_site | 14.6 ms                                                 | 16.3 ms: 1.11x slower                                                |
| Geometric mean         | (ref)                                                   | 1.09x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|-----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 46.9 ms                                                 | 64.3 ms: 1.37x slower                                                |
| genshi_text     | 31.7 ms                                                 | 43.7 ms: 1.38x slower                                                |
| mako            | 16.1 ms                                                 | 22.5 ms: 1.40x slower                                                |
| genshi_xml      | 68.3 ms                                                 | 101 ms: 1.48x slower                                                 |
| Geometric mean  | (ref)                                                   | 1.41x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle                   | 21.4 us                                                 | 19.4 us: 1.10x faster                                                |
| xml_etree_parse            | 236 ms                                                  | 223 ms: 1.06x faster                                                 |
| coverage                   | 110 ms                                                  | 114 ms: 1.04x slower                                                 |
| deepcopy_reduce            | 4.27 us                                                 | 4.47 us: 1.05x slower                                                |
| telco                      | 11.4 ms                                                 | 12.0 ms: 1.06x slower                                                |
| regex_dna                  | 288 ms                                                  | 304 ms: 1.06x slower                                                 |
| python_startup             | 22.0 ms                                                 | 23.5 ms: 1.07x slower                                                |
| meteor_contest             | 157 ms                                                  | 168 ms: 1.07x slower                                                 |
| async_tree_io_tg           | 1.46 sec                                                | 1.56 sec: 1.07x slower                                               |
| scimark_sparse_mat_mult    | 6.98 ms                                                 | 7.49 ms: 1.07x slower                                                |
| mdp                        | 3.80 sec                                                | 4.07 sec: 1.07x slower                                               |
| async_generators           | 592 ms                                                  | 637 ms: 1.08x slower                                                 |
| sqlite_synth               | 4.07 us                                                 | 4.40 us: 1.08x slower                                                |
| async_tree_memoization     | 745 ms                                                  | 809 ms: 1.09x slower                                                 |
| gc_traversal               | 5.91 ms                                                 | 6.46 ms: 1.09x slower                                                |
| xml_etree_generate         | 129 ms                                                  | 142 ms: 1.10x slower                                                 |
| async_tree_none            | 576 ms                                                  | 636 ms: 1.10x slower                                                 |
| xml_etree_iterparse        | 176 ms                                                  | 196 ms: 1.11x slower                                                 |
| python_startup_no_site     | 14.6 ms                                                 | 16.3 ms: 1.11x slower                                                |
| json_loads                 | 36.1 us                                                 | 40.3 us: 1.12x slower                                                |
| async_tree_cpu_io_mixed    | 899 ms                                                  | 1.01 sec: 1.12x slower                                               |
| json_dumps                 | 14.9 ms                                                 | 16.8 ms: 1.13x slower                                                |
| async_tree_io              | 1.38 sec                                                | 1.55 sec: 1.13x slower                                               |
| unpickle_list              | 6.67 us                                                 | 7.52 us: 1.13x slower                                                |
| docutils                   | 4.01 sec                                                | 4.52 sec: 1.13x slower                                               |
| scimark_fft                | 477 ms                                                  | 538 ms: 1.13x slower                                                 |
| async_tree_memoization_tg  | 672 ms                                                  | 760 ms: 1.13x slower                                                 |
| pathlib                    | 29.3 ms                                                 | 33.7 ms: 1.15x slower                                                |
| async_tree_none_tg         | 521 ms                                                  | 609 ms: 1.17x slower                                                 |
| json                       | 6.55 ms                                                 | 7.67 ms: 1.17x slower                                                |
| sympy_expand               | 631 ms                                                  | 742 ms: 1.18x slower                                                 |
| sympy_integrate            | 29.7 ms                                                 | 35.0 ms: 1.18x slower                                                |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 1.01 sec: 1.19x slower                                               |
| regex_v8                   | 32.4 ms                                                 | 38.6 ms: 1.19x slower                                                |
| pylint                     | 472 ms                                                  | 563 ms: 1.19x slower                                                 |
| bench_mp_pool              | 19.4 ms                                                 | 23.1 ms: 1.19x slower                                                |
| bpe_tokeniser              | 6.25 sec                                                | 7.57 sec: 1.21x slower                                               |
| sympy_sum                  | 213 ms                                                  | 260 ms: 1.22x slower                                                 |
| 2to3                       | 442 ms                                                  | 546 ms: 1.24x slower                                                 |
| generators                 | 39.2 ms                                                 | 48.5 ms: 1.24x slower                                                |
| nqueens                    | 108 ms                                                  | 136 ms: 1.26x slower                                                 |
| fannkuch                   | 543 ms                                                  | 688 ms: 1.27x slower                                                 |
| xml_etree_process          | 86.5 ms                                                 | 110 ms: 1.27x slower                                                 |
| typing_runtime_protocols   | 216 us                                                  | 275 us: 1.27x slower                                                 |
| thrift                     | 1.11 ms                                                 | 1.45 ms: 1.30x slower                                                |
| sympy_str                  | 367 ms                                                  | 480 ms: 1.31x slower                                                 |
| pycparser                  | 1.57 sec                                                | 2.06 sec: 1.31x slower                                               |
| html5lib                   | 98.1 ms                                                 | 130 ms: 1.32x slower                                                 |
| coroutines                 | 29.2 ms                                                 | 38.7 ms: 1.33x slower                                                |
| tomli_loads                | 2.80 sec                                                | 3.74 sec: 1.33x slower                                               |
| tornado_http               | 248 ms                                                  | 334 ms: 1.35x slower                                                 |
| spectral_norm              | 159 ms                                                  | 216 ms: 1.36x slower                                                 |
| bench_thread_pool          | 3.06 ms                                                 | 4.17 ms: 1.36x slower                                                |
| django_template            | 46.9 ms                                                 | 64.3 ms: 1.37x slower                                                |
| crypto_pyaes               | 99.8 ms                                                 | 137 ms: 1.37x slower                                                 |
| richards                   | 65.8 ms                                                 | 90.4 ms: 1.37x slower                                                |
| genshi_text                | 31.7 ms                                                 | 43.7 ms: 1.38x slower                                                |
| pprint_pformat             | 2.00 sec                                                | 2.76 sec: 1.38x slower                                               |
| sqlglot_optimize           | 76.2 ms                                                 | 106 ms: 1.39x slower                                                 |
| sqlglot_normalize          | 146 ms                                                  | 205 ms: 1.40x slower                                                 |
| mako                       | 16.1 ms                                                 | 22.5 ms: 1.40x slower                                                |
| regex_compile              | 177 ms                                                  | 253 ms: 1.42x slower                                                 |
| logging_simple             | 8.98 us                                                 | 12.9 us: 1.44x slower                                                |
| pprint_safe_repr           | 959 ms                                                  | 1.39 sec: 1.45x slower                                               |
| pyflate                    | 661 ms                                                  | 961 ms: 1.45x slower                                                 |
| richards_super             | 76.3 ms                                                 | 111 ms: 1.46x slower                                                 |
| comprehensions             | 20.9 us                                                 | 31.0 us: 1.48x slower                                                |
| genshi_xml                 | 68.3 ms                                                 | 101 ms: 1.48x slower                                                 |
| float                      | 115 ms                                                  | 171 ms: 1.49x slower                                                 |
| chaos                      | 84.7 ms                                                 | 129 ms: 1.52x slower                                                 |
| go                         | 195 ms                                                  | 298 ms: 1.52x slower                                                 |
| unpickle_pure_python       | 296 us                                                  | 461 us: 1.56x slower                                                 |
| sqlglot_transpile          | 2.30 ms                                                 | 3.66 ms: 1.59x slower                                                |
| pickle_pure_python         | 417 us                                                  | 673 us: 1.61x slower                                                 |
| logging_format             | 9.48 us                                                 | 15.4 us: 1.62x slower                                                |
| sqlglot_parse              | 1.80 ms                                                 | 2.93 ms: 1.63x slower                                                |
| scimark_monte_carlo        | 89.9 ms                                                 | 147 ms: 1.63x slower                                                 |
| logging_silent             | 130 ns                                                  | 214 ns: 1.64x slower                                                 |
| hexiom                     | 8.35 ms                                                 | 13.9 ms: 1.66x slower                                                |
| scimark_lu                 | 154 ms                                                  | 261 ms: 1.69x slower                                                 |
| raytrace                   | 350 ms                                                  | 608 ms: 1.74x slower                                                 |
| scimark_sor                | 172 ms                                                  | 304 ms: 1.76x slower                                                 |
| nbody                      | 124 ms                                                  | 226 ms: 1.82x slower                                                 |
| deltablue                  | 4.56 ms                                                 | 9.01 ms: 1.97x slower                                                |
| unpack_sequence            | 73.9 ns                                                 | 149 ns: 2.01x slower                                                 |
| Geometric mean             | (ref)                                                   | 1.25x slower                                                         |

Benchmark hidden because not significant (11): create_gc_cycles, pickle_dict, asyncio_websockets, pickle, pickle_list, asyncio_tcp, asyncio_tcp_ssl, regex_effbot, pidigits, deepcopy, deepcopy_memo
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.00x