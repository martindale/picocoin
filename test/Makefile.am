
INCLUDES	= @GLIB_CFLAGS@ -DTEST_SRCDIR=\"$(top_srcdir)/test\" \
		  -I$(top_srcdir)/include

EXTRA_DIST	= \
	base58_encode_decode.json	\
	base58_keys_valid.json		\
	random.data			\
	blk0.json  blk120383.json  tx3e0dc3da.json \
	blk0.ser  blk120383.ser  tx3e0dc3da.ser \
	blks10.ser \
	hdr193000.ser tn_hdr35141.ser \
	tn_blk35133.ser wallet-basics.json \
	script_valid.json script_invalid.json \
	tx_valid.json tx_invalid.json

noinst_LIBRARIES= libtest.a

libtest_a_SOURCES= libtest.h libtest.c

noinst_PROGRAMS	= hex base58 fileio util keyset bloom \
		  script-parse tx block blockfile blkdb script \
		  tx-valid wallet-basics chain-verf

TESTS		= hex base58 fileio util keyset bloom \
		  script-parse tx block blockfile blkdb script \
		  tx-valid wallet-basics chain-verf

COMMON_LDADD	= libtest.a ../lib/libccoin.a \
		  @GLIB_LIBS@ @CRYPTO_LIBS@ @JANSSON_LIBS@ @MATH_LIBS@

base58_LDADD		= $(COMMON_LDADD)
blkdb_LDADD		= $(COMMON_LDADD)
block_LDADD		= $(COMMON_LDADD)
blockfile_LDADD		= $(COMMON_LDADD)
bloom_LDADD		= $(COMMON_LDADD)
chain_verf_LDADD	= $(COMMON_LDADD)
fileio_LDADD		= $(COMMON_LDADD)
hex_LDADD		= $(COMMON_LDADD)
keyset_LDADD		= $(COMMON_LDADD)
script_LDADD		= $(COMMON_LDADD)
script_parse_LDADD	= $(COMMON_LDADD)
tx_LDADD		= $(COMMON_LDADD)
tx_valid_LDADD		= $(COMMON_LDADD)
util_LDADD		= $(COMMON_LDADD)
wallet_basics_LDADD	= $(COMMON_LDADD)

