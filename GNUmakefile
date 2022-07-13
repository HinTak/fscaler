include sources

CC=i686-w64-mingw32-gcc
CFLAGS=-flto -O3
LDFLAGS=-shared -Wl,--enable-stdcall-fixup -Wl,--enable-auto-image-base -Xlinker --out-implib -Xlinker $(TARGETNAME).dll.a

STRIP=i686-w64-mingw32-strip

default: $(TARGETNAME).dll

$(TARGETNAME).dll : $(TARGETNAME).def $(SOURCES)
	$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $^
	$(STRIP) $@

clean:
	$(RM) $(TARGETNAME).dll $(TARGETNAME).dll.a
