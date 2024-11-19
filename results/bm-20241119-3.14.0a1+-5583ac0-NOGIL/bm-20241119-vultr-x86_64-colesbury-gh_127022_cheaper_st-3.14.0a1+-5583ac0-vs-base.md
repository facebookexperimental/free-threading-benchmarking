# Results vs. base

- fork: colesbury
- ref: gh_127022_cheaper_st
- machine: linux-x86_64
- commit hash: 5583ac0
- commit date: 2024-11-19
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 419 ms                                                                 | 412 ms: 1.02x faster                                                      |
| html5lib       | 105 ms                                                                 | 106 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|--------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines         | 31.8 ms                                                                | 31.0 ms: 1.03x faster                                                     |
| asyncio_tcp_ssl    | 1.83 sec                                                               | 1.81 sec: 1.01x faster                                                    |
| asyncio_tcp        | 583 ms                                                                 | 580 ms: 1.01x faster                                                      |
| asyncio_websockets | 520 ms                                                                 | 518 ms: 1.00x faster                                                      |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 208 ms                                                                 | 199 ms: 1.05x faster                                                      |
| float          | 154 ms                                                                 | 150 ms: 1.03x faster                                                      |
| pidigits       | 183 ms                                                                 | 186 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 186 ms                                                                 | 180 ms: 1.04x faster                                                      |
| regex_compile  | 233 ms                                                                 | 228 ms: 1.02x faster                                                      |
| regex_v8       | 24.9 ms                                                                | 24.6 ms: 1.01x faster                                                     |
| regex_effbot   | 2.84 ms                                                                | 2.82 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pickle               | 12.4 us                                                                | 11.9 us: 1.04x faster                                                     |
| xml_etree_process    | 94.3 ms                                                                | 91.8 ms: 1.03x faster                                                     |
| tomli_loads          | 3.25 sec                                                               | 3.18 sec: 1.02x faster                                                    |
| pickle_dict          | 32.5 us                                                                | 31.9 us: 1.02x faster                                                     |
| xml_etree_generate   | 114 ms                                                                 | 112 ms: 1.02x faster                                                      |
| xml_etree_parse      | 134 ms                                                                 | 132 ms: 1.01x faster                                                      |
| xml_etree_iterparse  | 110 ms                                                                 | 109 ms: 1.01x faster                                                      |
| unpickle_pure_python | 425 us                                                                 | 422 us: 1.01x faster                                                      |
| pickle_pure_python   | 624 us                                                                 | 621 us: 1.00x faster                                                      |
| json_dumps           | 15.4 ms                                                                | 15.4 ms: 1.00x faster                                                     |
| pickle_list          | 5.11 us                                                                | 5.17 us: 1.01x slower                                                     |
| unpickle_list        | 5.01 us                                                                | 5.20 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (2): json_loads, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 15.7 ms                                                                | 15.6 ms: 1.00x faster                                                     |
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.00x faster                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 41.0 ms                                                                | 40.2 ms: 1.02x faster                                                     |
| django_template | 65.7 ms                                                                | 64.4 ms: 1.02x faster                                                     |
| mako            | 21.1 ms                                                                | 20.7 ms: 1.02x faster                                                     |
| genshi_xml      | 82.8 ms                                                                | 81.5 ms: 1.02x faster                                                     |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                              |

All benchmarks:
===============

| Benchmark               | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| gc_traversal            | 2.59 ms                                                                | 2.36 ms: 1.09x faster                                                     |
| nbody                   | 208 ms                                                                 | 199 ms: 1.05x faster                                                      |
| pickle                  | 12.4 us                                                                | 11.9 us: 1.04x faster                                                     |
| mdp                     | 3.18 sec                                                               | 3.05 sec: 1.04x faster                                                    |
| raytrace                | 644 ms                                                                 | 618 ms: 1.04x faster                                                      |
| sqlglot_parse           | 2.95 ms                                                                | 2.84 ms: 1.04x faster                                                     |
| deepcopy_reduce         | 4.60 us                                                                | 4.43 us: 1.04x faster                                                     |
| regex_dna               | 186 ms                                                                 | 180 ms: 1.04x faster                                                      |
| spectral_norm           | 167 ms                                                                 | 161 ms: 1.04x faster                                                      |
| scimark_fft             | 431 ms                                                                 | 417 ms: 1.04x faster                                                      |
| scimark_monte_carlo     | 130 ms                                                                 | 126 ms: 1.03x faster                                                      |
| chaos                   | 124 ms                                                                 | 121 ms: 1.03x faster                                                      |
| xml_etree_process       | 94.3 ms                                                                | 91.8 ms: 1.03x faster                                                     |
| scimark_lu              | 254 ms                                                                 | 247 ms: 1.03x faster                                                      |
| coroutines              | 31.8 ms                                                                | 31.0 ms: 1.03x faster                                                     |
| logging_silent          | 217 ns                                                                 | 212 ns: 1.03x faster                                                      |
| comprehensions          | 31.1 us                                                                | 30.3 us: 1.03x faster                                                     |
| float                   | 154 ms                                                                 | 150 ms: 1.03x faster                                                      |
| generators              | 41.2 ms                                                                | 40.2 ms: 1.03x faster                                                     |
| thrift                  | 1.29 ms                                                                | 1.26 ms: 1.03x faster                                                     |
| crypto_pyaes            | 110 ms                                                                 | 108 ms: 1.02x faster                                                      |
| unpack_sequence         | 150 ns                                                                 | 147 ns: 1.02x faster                                                      |
| tomli_loads             | 3.25 sec                                                               | 3.18 sec: 1.02x faster                                                    |
| genshi_text             | 41.0 ms                                                                | 40.2 ms: 1.02x faster                                                     |
| django_template         | 65.7 ms                                                                | 64.4 ms: 1.02x faster                                                     |
| regex_compile           | 233 ms                                                                 | 228 ms: 1.02x faster                                                      |
| logging_format          | 13.5 us                                                                | 13.2 us: 1.02x faster                                                     |
| pprint_safe_repr        | 1.34 sec                                                               | 1.32 sec: 1.02x faster                                                    |
| pickle_dict             | 32.5 us                                                                | 31.9 us: 1.02x faster                                                     |
| deepcopy                | 439 us                                                                 | 431 us: 1.02x faster                                                      |
| deltablue               | 9.27 ms                                                                | 9.10 ms: 1.02x faster                                                     |
| xml_etree_generate      | 114 ms                                                                 | 112 ms: 1.02x faster                                                      |
| meteor_contest          | 141 ms                                                                 | 138 ms: 1.02x faster                                                      |
| sqlglot_transpile       | 3.37 ms                                                                | 3.31 ms: 1.02x faster                                                     |
| hexiom                  | 12.7 ms                                                                | 12.4 ms: 1.02x faster                                                     |
| logging_simple          | 12.1 us                                                                | 11.9 us: 1.02x faster                                                     |
| mako                    | 21.1 ms                                                                | 20.7 ms: 1.02x faster                                                     |
| scimark_sor             | 273 ms                                                                 | 269 ms: 1.02x faster                                                      |
| 2to3                    | 419 ms                                                                 | 412 ms: 1.02x faster                                                      |
| genshi_xml              | 82.8 ms                                                                | 81.5 ms: 1.02x faster                                                     |
| xml_etree_parse         | 134 ms                                                                 | 132 ms: 1.01x faster                                                      |
| nqueens                 | 116 ms                                                                 | 115 ms: 1.01x faster                                                      |
| richards_super          | 110 ms                                                                 | 109 ms: 1.01x faster                                                      |
| sqlglot_normalize       | 183 ms                                                                 | 180 ms: 1.01x faster                                                      |
| sqlite_synth            | 2.45 us                                                                | 2.42 us: 1.01x faster                                                     |
| pycparser               | 1.72 sec                                                               | 1.69 sec: 1.01x faster                                                    |
| go                      | 306 ms                                                                 | 303 ms: 1.01x faster                                                      |
| xml_etree_iterparse     | 110 ms                                                                 | 109 ms: 1.01x faster                                                      |
| asyncio_tcp_ssl         | 1.83 sec                                                               | 1.81 sec: 1.01x faster                                                    |
| sqlglot_optimize        | 91.6 ms                                                                | 90.7 ms: 1.01x faster                                                     |
| sympy_expand            | 1.06 sec                                                               | 1.05 sec: 1.01x faster                                                    |
| regex_v8                | 24.9 ms                                                                | 24.6 ms: 1.01x faster                                                     |
| pyflate                 | 785 ms                                                                 | 778 ms: 1.01x faster                                                      |
| deepcopy_memo           | 53.3 us                                                                | 52.9 us: 1.01x faster                                                     |
| pathlib                 | 21.9 ms                                                                | 21.7 ms: 1.01x faster                                                     |
| pprint_pformat          | 2.77 sec                                                               | 2.74 sec: 1.01x faster                                                    |
| unpickle_pure_python    | 425 us                                                                 | 422 us: 1.01x faster                                                      |
| sympy_str               | 544 ms                                                                 | 540 ms: 1.01x faster                                                      |
| json                    | 5.31 ms                                                                | 5.27 ms: 1.01x faster                                                     |
| telco                   | 9.47 ms                                                                | 9.42 ms: 1.01x faster                                                     |
| sympy_integrate         | 33.3 ms                                                                | 33.1 ms: 1.01x faster                                                     |
| regex_effbot            | 2.84 ms                                                                | 2.82 ms: 1.01x faster                                                     |
| asyncio_tcp             | 583 ms                                                                 | 580 ms: 1.01x faster                                                      |
| pickle_pure_python      | 624 us                                                                 | 621 us: 1.00x faster                                                      |
| bench_thread_pool       | 3.51 ms                                                                | 3.49 ms: 1.00x faster                                                     |
| json_dumps              | 15.4 ms                                                                | 15.4 ms: 1.00x faster                                                     |
| dulwich_log             | 103 ms                                                                 | 103 ms: 1.00x faster                                                      |
| asyncio_websockets      | 520 ms                                                                 | 518 ms: 1.00x faster                                                      |
| python_startup          | 15.7 ms                                                                | 15.6 ms: 1.00x faster                                                     |
| python_startup_no_site  | 10.3 ms                                                                | 10.2 ms: 1.00x faster                                                     |
| html5lib                | 105 ms                                                                 | 106 ms: 1.01x slower                                                      |
| pickle_list             | 5.11 us                                                                | 5.17 us: 1.01x slower                                                     |
| pidigits                | 183 ms                                                                 | 186 ms: 1.02x slower                                                      |
| fannkuch                | 563 ms                                                                 | 572 ms: 1.02x slower                                                      |
| scimark_sparse_mat_mult | 5.85 ms                                                                | 5.95 ms: 1.02x slower                                                     |
| unpickle_list           | 5.01 us                                                                | 5.20 us: 1.04x slower                                                     |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (12): pylint, async_generators, json_loads, bench_mp_pool, sympy_sum, typing_runtime_protocols, docutils, bpe_tokeniser, coverage, richards, unpickle, create_gc_cycles

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x