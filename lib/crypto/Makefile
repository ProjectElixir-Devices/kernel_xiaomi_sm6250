# SPDX-License-Identifier: GPL-2.0

obj-$(CONFIG_CRYPTO_LIB_CURVE25519_GENERIC)	+= libcurve25519.o
libcurve25519-y					:= curve25519-fiat32.o
libcurve25519-$(CONFIG_ARCH_SUPPORTS_INT128)	:= curve25519-hacl64.o
libcurve25519-y					+= curve25519.o

obj-y += libblake2s.o
libblake2s-y += blake2s.o blake2s-generic.o
ifneq ($(CONFIG_CRYPTO_MANAGER_DISABLE_TESTS),y)
libblake2s-y += blake2s-selftest.o
endif
