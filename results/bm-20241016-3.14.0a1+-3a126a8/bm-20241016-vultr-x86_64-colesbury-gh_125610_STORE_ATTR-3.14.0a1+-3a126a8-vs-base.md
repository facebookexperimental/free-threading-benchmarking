# Results vs. base

- fork: colesbury
- ref: gh_125610_STORE_ATTR
- machine: linux-x86_64
- commit hash: 3a126a8
- commit date: 2024-10-16
- overall geometric mean: 1.00x slower
- HPT reliability: 98.84%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 253 ms: 1.00x slower                                                      |
| docutils       | 2.57 sec                                                               | 2.60 sec: 1.01x slower                                                    |
| html5lib       | 62.4 ms                                                                | 63.7 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines       | 22.4 ms                                                                | 22.1 ms: 1.01x faster                                                     |
| async_generators | 373 ms                                                                 | 371 ms: 1.00x faster                                                      |
| Geometric mean   | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (3): asyncio_websockets, asyncio_tcp_ssl, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 79.5 ms                                                                | 78.9 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 176 ms                                                                 | 183 ms: 1.03x slower                                                      |
| regex_v8       | 23.0 ms                                                                | 24.2 ms: 1.05x slower                                                     |
| regex_effbot   | 2.95 ms                                                                | 3.19 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                              |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle_list        | 4.71 us                                                                | 4.61 us: 1.02x faster                                                     |
| unpickle             | 13.5 us                                                                | 13.2 us: 1.02x faster                                                     |
| json_loads           | 26.3 us                                                                | 25.9 us: 1.02x faster                                                     |
| tomli_loads          | 2.10 sec                                                               | 2.09 sec: 1.01x faster                                                    |
| xml_etree_generate   | 85.3 ms                                                                | 84.9 ms: 1.00x faster                                                     |
| unpickle_pure_python | 214 us                                                                 | 215 us: 1.01x slower                                                      |
| json_dumps           | 11.6 ms                                                                | 11.7 ms: 1.01x slower                                                     |
| pickle_list          | 4.85 us                                                                | 5.10 us: 1.05x slower                                                     |
| pickle_dict          | 30.9 us                                                                | 33.0 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (5): pickle, pickle_pure_python, xml_etree_process, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 22.7 ms                                                                | 22.2 ms: 1.02x faster                                                     |
| django_template | 35.9 ms                                                                | 35.2 ms: 1.02x faster                                                     |
| mako            | 11.6 ms                                                                | 11.8 ms: 1.02x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|--------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpack_sequence          | 53.1 ns                                                                | 42.1 ns: 1.26x faster                                                     |
| gc_traversal             | 3.46 ms                                                                | 3.26 ms: 1.06x faster                                                     |
| richards                 | 46.1 ms                                                                | 44.9 ms: 1.03x faster                                                     |
| deepcopy_reduce          | 2.68 us                                                                | 2.62 us: 1.02x faster                                                     |
| unpickle_list            | 4.71 us                                                                | 4.61 us: 1.02x faster                                                     |
| genshi_text              | 22.7 ms                                                                | 22.2 ms: 1.02x faster                                                     |
| django_template          | 35.9 ms                                                                | 35.2 ms: 1.02x faster                                                     |
| go                       | 120 ms                                                                 | 118 ms: 1.02x faster                                                      |
| raytrace                 | 264 ms                                                                 | 260 ms: 1.02x faster                                                      |
| richards_super           | 51.7 ms                                                                | 50.8 ms: 1.02x faster                                                     |
| unpickle                 | 13.5 us                                                                | 13.2 us: 1.02x faster                                                     |
| json_loads               | 26.3 us                                                                | 25.9 us: 1.02x faster                                                     |
| coroutines               | 22.4 ms                                                                | 22.1 ms: 1.01x faster                                                     |
| hexiom                   | 5.98 ms                                                                | 5.91 ms: 1.01x faster                                                     |
| meteor_contest           | 103 ms                                                                 | 102 ms: 1.01x faster                                                      |
| json                     | 4.92 ms                                                                | 4.87 ms: 1.01x faster                                                     |
| deepcopy                 | 263 us                                                                 | 260 us: 1.01x faster                                                      |
| sqlglot_parse            | 1.30 ms                                                                | 1.29 ms: 1.01x faster                                                     |
| generators               | 28.7 ms                                                                | 28.4 ms: 1.01x faster                                                     |
| typing_runtime_protocols | 158 us                                                                 | 157 us: 1.01x faster                                                      |
| logging_format           | 6.80 us                                                                | 6.75 us: 1.01x faster                                                     |
| tomli_loads              | 2.10 sec                                                               | 2.09 sec: 1.01x faster                                                    |
| float                    | 79.5 ms                                                                | 78.9 ms: 1.01x faster                                                     |
| sqlglot_transpile        | 1.60 ms                                                                | 1.59 ms: 1.01x faster                                                     |
| xml_etree_generate       | 85.3 ms                                                                | 84.9 ms: 1.00x faster                                                     |
| async_generators         | 373 ms                                                                 | 371 ms: 1.00x faster                                                      |
| sqlglot_optimize         | 53.5 ms                                                                | 53.4 ms: 1.00x faster                                                     |
| bpe_tokeniser            | 4.36 sec                                                               | 4.35 sec: 1.00x faster                                                    |
| 2to3                     | 253 ms                                                                 | 253 ms: 1.00x slower                                                      |
| sympy_integrate          | 19.9 ms                                                                | 20.0 ms: 1.00x slower                                                     |
| sqlglot_normalize        | 106 ms                                                                 | 106 ms: 1.01x slower                                                      |
| deltablue                | 3.19 ms                                                                | 3.21 ms: 1.01x slower                                                     |
| unpickle_pure_python     | 214 us                                                                 | 215 us: 1.01x slower                                                      |
| deepcopy_memo            | 30.2 us                                                                | 30.4 us: 1.01x slower                                                     |
| pyflate                  | 454 ms                                                                 | 457 ms: 1.01x slower                                                      |
| nqueens                  | 78.3 ms                                                                | 78.9 ms: 1.01x slower                                                     |
| pprint_safe_repr         | 710 ms                                                                 | 716 ms: 1.01x slower                                                      |
| scimark_fft              | 342 ms                                                                 | 345 ms: 1.01x slower                                                      |
| comprehensions           | 16.9 us                                                                | 17.0 us: 1.01x slower                                                     |
| dulwich_log              | 74.1 ms                                                                | 74.8 ms: 1.01x slower                                                     |
| pycparser                | 1.20 sec                                                               | 1.21 sec: 1.01x slower                                                    |
| docutils                 | 2.57 sec                                                               | 2.60 sec: 1.01x slower                                                    |
| scimark_monte_carlo      | 65.7 ms                                                                | 66.3 ms: 1.01x slower                                                     |
| json_dumps               | 11.6 ms                                                                | 11.7 ms: 1.01x slower                                                     |
| scimark_sor              | 133 ms                                                                 | 135 ms: 1.01x slower                                                      |
| sympy_expand             | 456 ms                                                                 | 461 ms: 1.01x slower                                                      |
| sqlite_synth             | 2.21 us                                                                | 2.23 us: 1.01x slower                                                     |
| fannkuch                 | 382 ms                                                                 | 387 ms: 1.01x slower                                                      |
| telco                    | 7.34 ms                                                                | 7.45 ms: 1.02x slower                                                     |
| spectral_norm            | 108 ms                                                                 | 109 ms: 1.02x slower                                                      |
| pathlib                  | 18.5 ms                                                                | 18.7 ms: 1.02x slower                                                     |
| crypto_pyaes             | 66.6 ms                                                                | 67.7 ms: 1.02x slower                                                     |
| mako                     | 11.6 ms                                                                | 11.8 ms: 1.02x slower                                                     |
| html5lib                 | 62.4 ms                                                                | 63.7 ms: 1.02x slower                                                     |
| regex_dna                | 176 ms                                                                 | 183 ms: 1.03x slower                                                      |
| scimark_lu               | 110 ms                                                                 | 115 ms: 1.05x slower                                                      |
| regex_v8                 | 23.0 ms                                                                | 24.2 ms: 1.05x slower                                                     |
| pickle_list              | 4.85 us                                                                | 5.10 us: 1.05x slower                                                     |
| pickle_dict              | 30.9 us                                                                | 33.0 us: 1.07x slower                                                     |
| regex_effbot             | 2.95 ms                                                                | 3.19 ms: 1.08x slower                                                     |
| scimark_sparse_mat_mult  | 4.33 ms                                                                | 4.70 ms: 1.08x slower                                                     |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (28): pickle, thrift, pickle_pure_python, logging_silent, create_gc_cycles, genshi_xml, chaos, bench_mp_pool, pidigits, asyncio_websockets, python_startup_no_site, pylint, regex_compile, python_startup, coverage, bench_thread_pool, asyncio_tcp_ssl, mdp, pprint_pformat, xml_etree_process, sympy_sum, sympy_str, xml_etree_parse, xml_etree_iterparse, asyncio_tcp, tornado_http, logging_simple, nbody

# HPT report

- Reliability score: 98.84% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x