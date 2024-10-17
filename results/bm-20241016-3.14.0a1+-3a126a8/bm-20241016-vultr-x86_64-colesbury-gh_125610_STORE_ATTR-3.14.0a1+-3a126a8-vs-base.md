# Results vs. base

- fork: colesbury
- ref: gh_125610_STORE_ATTR
- machine: linux-x86_64
- commit hash: 3a126a8
- commit date: 2024-10-16
- overall geometric mean: 1.01x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 255 ms: 1.01x slower                                                      |
| docutils       | 2.57 sec                                                               | 2.61 sec: 1.01x slower                                                    |
| html5lib       | 62.4 ms                                                                | 63.1 ms: 1.01x slower                                                     |
| tornado_http   | 113 ms                                                                 | 114 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_generators | 373 ms                                                                 | 371 ms: 1.00x faster                                                      |
| Geometric mean   | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (4): coroutines, asyncio_websockets, asyncio_tcp_ssl, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 79.5 ms                                                                | 79.8 ms: 1.00x slower                                                     |
| pidigits       | 185 ms                                                                 | 186 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 176 ms                                                                 | 179 ms: 1.01x slower                                                      |
| regex_effbot   | 2.95 ms                                                                | 3.01 ms: 1.02x slower                                                     |
| regex_v8       | 23.0 ms                                                                | 24.5 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                              |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pickle_pure_python   | 308 us                                                                 | 307 us: 1.00x faster                                                      |
| xml_etree_generate   | 85.3 ms                                                                | 85.0 ms: 1.00x faster                                                     |
| xml_etree_process    | 59.2 ms                                                                | 59.4 ms: 1.00x slower                                                     |
| json_dumps           | 11.6 ms                                                                | 11.6 ms: 1.01x slower                                                     |
| xml_etree_iterparse  | 95.7 ms                                                                | 96.4 ms: 1.01x slower                                                     |
| xml_etree_parse      | 136 ms                                                                 | 138 ms: 1.02x slower                                                      |
| unpickle_pure_python | 214 us                                                                 | 218 us: 1.02x slower                                                      |
| unpickle             | 13.5 us                                                                | 13.8 us: 1.02x slower                                                     |
| pickle_list          | 4.85 us                                                                | 5.03 us: 1.04x slower                                                     |
| unpickle_list        | 4.71 us                                                                | 4.89 us: 1.04x slower                                                     |
| pickle_dict          | 30.9 us                                                                | 34.0 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                              |

Benchmark hidden because not significant (3): json_loads, tomli_loads, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.47 ms: 1.01x slower                                                     |
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 22.7 ms                                                                | 22.3 ms: 1.01x faster                                                     |
| django_template | 35.9 ms                                                                | 35.4 ms: 1.01x faster                                                     |
| mako            | 11.6 ms                                                                | 11.7 ms: 1.01x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1+-760872e | bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1+-3a126a8 |
|--------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                                | 3.30 ms: 1.05x faster                                                     |
| unpack_sequence          | 53.1 ns                                                                | 51.0 ns: 1.04x faster                                                     |
| typing_runtime_protocols | 158 us                                                                 | 156 us: 1.02x faster                                                      |
| fannkuch                 | 382 ms                                                                 | 376 ms: 1.02x faster                                                      |
| genshi_text              | 22.7 ms                                                                | 22.3 ms: 1.01x faster                                                     |
| django_template          | 35.9 ms                                                                | 35.4 ms: 1.01x faster                                                     |
| sqlglot_parse            | 1.30 ms                                                                | 1.29 ms: 1.01x faster                                                     |
| deepcopy_memo            | 30.2 us                                                                | 30.0 us: 1.01x faster                                                     |
| deepcopy_reduce          | 2.68 us                                                                | 2.66 us: 1.01x faster                                                     |
| pickle_pure_python       | 308 us                                                                 | 307 us: 1.00x faster                                                      |
| async_generators         | 373 ms                                                                 | 371 ms: 1.00x faster                                                      |
| sqlglot_transpile        | 1.60 ms                                                                | 1.59 ms: 1.00x faster                                                     |
| xml_etree_generate       | 85.3 ms                                                                | 85.0 ms: 1.00x faster                                                     |
| nqueens                  | 78.3 ms                                                                | 78.6 ms: 1.00x slower                                                     |
| xml_etree_process        | 59.2 ms                                                                | 59.4 ms: 1.00x slower                                                     |
| float                    | 79.5 ms                                                                | 79.8 ms: 1.00x slower                                                     |
| mako                     | 11.6 ms                                                                | 11.7 ms: 1.01x slower                                                     |
| pidigits                 | 185 ms                                                                 | 186 ms: 1.01x slower                                                      |
| chaos                    | 59.3 ms                                                                | 59.6 ms: 1.01x slower                                                     |
| json_dumps               | 11.6 ms                                                                | 11.6 ms: 1.01x slower                                                     |
| xml_etree_iterparse      | 95.7 ms                                                                | 96.4 ms: 1.01x slower                                                     |
| sympy_expand             | 456 ms                                                                 | 460 ms: 1.01x slower                                                      |
| raytrace                 | 264 ms                                                                 | 266 ms: 1.01x slower                                                      |
| pyflate                  | 454 ms                                                                 | 458 ms: 1.01x slower                                                      |
| python_startup_no_site   | 7.41 ms                                                                | 7.47 ms: 1.01x slower                                                     |
| pycparser                | 1.20 sec                                                               | 1.21 sec: 1.01x slower                                                    |
| pathlib                  | 18.5 ms                                                                | 18.6 ms: 1.01x slower                                                     |
| scimark_fft              | 342 ms                                                                 | 346 ms: 1.01x slower                                                      |
| 2to3                     | 253 ms                                                                 | 255 ms: 1.01x slower                                                      |
| bpe_tokeniser            | 4.36 sec                                                               | 4.41 sec: 1.01x slower                                                    |
| sympy_sum                | 154 ms                                                                 | 155 ms: 1.01x slower                                                      |
| bench_mp_pool            | 63.3 ms                                                                | 64.0 ms: 1.01x slower                                                     |
| meteor_contest           | 103 ms                                                                 | 104 ms: 1.01x slower                                                      |
| sympy_integrate          | 19.9 ms                                                                | 20.1 ms: 1.01x slower                                                     |
| logging_simple           | 6.04 us                                                                | 6.10 us: 1.01x slower                                                     |
| sympy_str                | 271 ms                                                                 | 274 ms: 1.01x slower                                                      |
| generators               | 28.7 ms                                                                | 29.0 ms: 1.01x slower                                                     |
| html5lib                 | 62.4 ms                                                                | 63.1 ms: 1.01x slower                                                     |
| telco                    | 7.34 ms                                                                | 7.43 ms: 1.01x slower                                                     |
| scimark_monte_carlo      | 65.7 ms                                                                | 66.5 ms: 1.01x slower                                                     |
| dulwich_log              | 74.1 ms                                                                | 75.0 ms: 1.01x slower                                                     |
| thrift                   | 753 us                                                                 | 762 us: 1.01x slower                                                      |
| hexiom                   | 5.98 ms                                                                | 6.05 ms: 1.01x slower                                                     |
| python_startup           | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                                     |
| create_gc_cycles         | 1.36 ms                                                                | 1.38 ms: 1.01x slower                                                     |
| richards                 | 46.1 ms                                                                | 46.7 ms: 1.01x slower                                                     |
| regex_dna                | 176 ms                                                                 | 179 ms: 1.01x slower                                                      |
| tornado_http             | 113 ms                                                                 | 114 ms: 1.01x slower                                                      |
| docutils                 | 2.57 sec                                                               | 2.61 sec: 1.01x slower                                                    |
| richards_super           | 51.7 ms                                                                | 52.4 ms: 1.02x slower                                                     |
| xml_etree_parse          | 136 ms                                                                 | 138 ms: 1.02x slower                                                      |
| go                       | 120 ms                                                                 | 122 ms: 1.02x slower                                                      |
| comprehensions           | 16.9 us                                                                | 17.2 us: 1.02x slower                                                     |
| unpickle_pure_python     | 214 us                                                                 | 218 us: 1.02x slower                                                      |
| regex_effbot             | 2.95 ms                                                                | 3.01 ms: 1.02x slower                                                     |
| scimark_lu               | 110 ms                                                                 | 113 ms: 1.02x slower                                                      |
| scimark_sor              | 133 ms                                                                 | 137 ms: 1.02x slower                                                      |
| unpickle                 | 13.5 us                                                                | 13.8 us: 1.02x slower                                                     |
| deltablue                | 3.19 ms                                                                | 3.28 ms: 1.03x slower                                                     |
| logging_silent           | 103 ns                                                                 | 106 ns: 1.03x slower                                                      |
| pickle_list              | 4.85 us                                                                | 5.03 us: 1.04x slower                                                     |
| unpickle_list            | 4.71 us                                                                | 4.89 us: 1.04x slower                                                     |
| crypto_pyaes             | 66.6 ms                                                                | 69.1 ms: 1.04x slower                                                     |
| spectral_norm            | 108 ms                                                                 | 113 ms: 1.05x slower                                                      |
| scimark_sparse_mat_mult  | 4.33 ms                                                                | 4.62 ms: 1.07x slower                                                     |
| regex_v8                 | 23.0 ms                                                                | 24.5 ms: 1.07x slower                                                     |
| pickle_dict              | 30.9 us                                                                | 34.0 us: 1.10x slower                                                     |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (22): sqlite_synth, nbody, pprint_pformat, regex_compile, coroutines, json_loads, tomli_loads, asyncio_websockets, sqlglot_optimize, asyncio_tcp_ssl, sqlglot_normalize, asyncio_tcp, pickle, deepcopy, coverage, genshi_xml, json, mdp, bench_thread_pool, pprint_safe_repr, logging_format, pylint

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x