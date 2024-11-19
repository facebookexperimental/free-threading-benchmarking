# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: e051157
- commit date: 2024-11-18
- overall geometric mean: 1.00x faster
- HPT reliability: 98.27%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 420 ms                                                                 | 417 ms: 1.01x faster                                                  |
| docutils       | 3.40 sec                                                               | 3.38 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines     | 31.2 ms                                                                | 31.5 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (4): asyncio_tcp_ssl, asyncio_tcp, async_generators, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 152 ms                                                                 | 153 ms: 1.01x slower                                                  |
| pidigits       | 183 ms                                                                 | 185 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.96 ms                                                                | 2.99 ms: 1.01x slower                                                 |
| regex_dna      | 184 ms                                                                 | 189 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 429 us                                                                 | 423 us: 1.01x faster                                                  |
| xml_etree_generate   | 115 ms                                                                 | 113 ms: 1.01x faster                                                  |
| pickle_pure_python   | 630 us                                                                 | 622 us: 1.01x faster                                                  |
| pickle_dict          | 32.4 us                                                                | 32.0 us: 1.01x faster                                                 |
| xml_etree_process    | 94.1 ms                                                                | 93.4 ms: 1.01x faster                                                 |
| tomli_loads          | 3.25 sec                                                               | 3.24 sec: 1.00x faster                                                |
| pickle_list          | 5.20 us                                                                | 5.23 us: 1.01x slower                                                 |
| xml_etree_parse      | 134 ms                                                                 | 135 ms: 1.01x slower                                                  |
| unpickle_list        | 4.88 us                                                                | 5.06 us: 1.04x slower                                                 |
| pickle               | 12.4 us                                                                | 13.5 us: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (4): xml_etree_iterparse, json_loads, unpickle, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                 |
| python_startup         | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 66.5 ms                                                                | 64.9 ms: 1.03x faster                                                 |
| genshi_xml      | 84.0 ms                                                                | 82.9 ms: 1.01x faster                                                 |
| mako            | 21.1 ms                                                                | 20.8 ms: 1.01x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|--------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpack_sequence          | 156 ns                                                                 | 142 ns: 1.10x faster                                                  |
| meteor_contest           | 140 ms                                                                 | 137 ms: 1.03x faster                                                  |
| django_template          | 66.5 ms                                                                | 64.9 ms: 1.03x faster                                                 |
| spectral_norm            | 163 ms                                                                 | 159 ms: 1.02x faster                                                  |
| pathlib                  | 22.1 ms                                                                | 21.7 ms: 1.02x faster                                                 |
| richards                 | 93.3 ms                                                                | 91.6 ms: 1.02x faster                                                 |
| logging_simple           | 12.4 us                                                                | 12.2 us: 1.01x faster                                                 |
| unpickle_pure_python     | 429 us                                                                 | 423 us: 1.01x faster                                                  |
| sqlglot_normalize        | 184 ms                                                                 | 182 ms: 1.01x faster                                                  |
| xml_etree_generate       | 115 ms                                                                 | 113 ms: 1.01x faster                                                  |
| genshi_xml               | 84.0 ms                                                                | 82.9 ms: 1.01x faster                                                 |
| pickle_pure_python       | 630 us                                                                 | 622 us: 1.01x faster                                                  |
| logging_silent           | 219 ns                                                                 | 216 ns: 1.01x faster                                                  |
| pickle_dict              | 32.4 us                                                                | 32.0 us: 1.01x faster                                                 |
| mako                     | 21.1 ms                                                                | 20.8 ms: 1.01x faster                                                 |
| pycparser                | 1.75 sec                                                               | 1.73 sec: 1.01x faster                                                |
| deepcopy                 | 437 us                                                                 | 433 us: 1.01x faster                                                  |
| deepcopy_memo            | 54.1 us                                                                | 53.6 us: 1.01x faster                                                 |
| pyflate                  | 793 ms                                                                 | 786 ms: 1.01x faster                                                  |
| xml_etree_process        | 94.1 ms                                                                | 93.4 ms: 1.01x faster                                                 |
| comprehensions           | 30.9 us                                                                | 30.6 us: 1.01x faster                                                 |
| telco                    | 9.36 ms                                                                | 9.29 ms: 1.01x faster                                                 |
| coverage                 | 103 ms                                                                 | 102 ms: 1.01x faster                                                  |
| hexiom                   | 12.6 ms                                                                | 12.5 ms: 1.01x faster                                                 |
| fannkuch                 | 568 ms                                                                 | 564 ms: 1.01x faster                                                  |
| docutils                 | 3.40 sec                                                               | 3.38 sec: 1.01x faster                                                |
| 2to3                     | 420 ms                                                                 | 417 ms: 1.01x faster                                                  |
| sympy_expand             | 1.07 sec                                                               | 1.06 sec: 1.01x faster                                                |
| sympy_str                | 546 ms                                                                 | 543 ms: 1.01x faster                                                  |
| tomli_loads              | 3.25 sec                                                               | 3.24 sec: 1.00x faster                                                |
| sympy_sum                | 384 ms                                                                 | 382 ms: 1.00x faster                                                  |
| nqueens                  | 116 ms                                                                 | 116 ms: 1.00x faster                                                  |
| python_startup_no_site   | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                 |
| python_startup           | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                                 |
| crypto_pyaes             | 109 ms                                                                 | 109 ms: 1.00x faster                                                  |
| deltablue                | 9.22 ms                                                                | 9.26 ms: 1.00x slower                                                 |
| float                    | 152 ms                                                                 | 153 ms: 1.01x slower                                                  |
| sqlglot_parse            | 2.86 ms                                                                | 2.88 ms: 1.01x slower                                                 |
| pickle_list              | 5.20 us                                                                | 5.23 us: 1.01x slower                                                 |
| go                       | 300 ms                                                                 | 301 ms: 1.01x slower                                                  |
| create_gc_cycles         | 1.14 ms                                                                | 1.15 ms: 1.01x slower                                                 |
| typing_runtime_protocols | 250 us                                                                 | 252 us: 1.01x slower                                                  |
| pidigits                 | 183 ms                                                                 | 185 ms: 1.01x slower                                                  |
| mdp                      | 3.14 sec                                                               | 3.16 sec: 1.01x slower                                                |
| coroutines               | 31.2 ms                                                                | 31.5 ms: 1.01x slower                                                 |
| xml_etree_parse          | 134 ms                                                                 | 135 ms: 1.01x slower                                                  |
| scimark_monte_carlo      | 128 ms                                                                 | 130 ms: 1.01x slower                                                  |
| regex_effbot             | 2.96 ms                                                                | 2.99 ms: 1.01x slower                                                 |
| scimark_fft              | 420 ms                                                                 | 425 ms: 1.01x slower                                                  |
| sqlite_synth             | 2.43 us                                                                | 2.47 us: 1.02x slower                                                 |
| raytrace                 | 632 ms                                                                 | 647 ms: 1.02x slower                                                  |
| regex_dna                | 184 ms                                                                 | 189 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult  | 5.87 ms                                                                | 6.05 ms: 1.03x slower                                                 |
| richards_super           | 110 ms                                                                 | 113 ms: 1.03x slower                                                  |
| unpickle_list            | 4.88 us                                                                | 5.06 us: 1.04x slower                                                 |
| pickle                   | 12.4 us                                                                | 13.5 us: 1.09x slower                                                 |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (32): asyncio_tcp_ssl, xml_etree_iterparse, pprint_safe_repr, html5lib, thrift, pylint, scimark_sor, sqlglot_optimize, pprint_pformat, regex_compile, bench_thread_pool, genshi_text, bench_mp_pool, json, sympy_integrate, json_loads, nbody, chaos, dulwich_log, generators, asyncio_tcp, async_generators, unpickle, asyncio_websockets, bpe_tokeniser, deepcopy_reduce, regex_v8, gc_traversal, sqlglot_transpile, logging_format, json_dumps, scimark_lu

# HPT report

- Reliability score: 98.27% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x