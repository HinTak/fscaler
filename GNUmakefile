include sources

CC=i686-w64-mingw32-gcc
CFLAGS=-flto -O3
LDFLAGS=-shared -Wl,--enable-stdcall-fixup -Wl,--enable-auto-image-base -Xlinker --out-implib -Xlinker $(TARGETNAME).dll.a

default: $(TARGETNAME).dll

$(TARGETNAME).dll : $(TARGETNAME).def
	$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $^ $(SOURCES)

clean:
	$(RM) $(TARGETNAME).dll $(TARGETNAME).dll.a
