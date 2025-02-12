## MY NASRAL##

--wf-tcp=80,443 --wf-udp=443,50000-50099 ^
--filter-udp=50000-50099 --ipset="/opt/zapret/ipset-discord.txt" --dpi-desync=fake --dpi-desync-repeats=6 --dpi-desync-any-protocol --dpi-desync-cutoff=n2 --new
--filter-udp=50000-50099 --new
--filter-udp=443 --hostlist="/opt/zapret/list-youtube.txt" --dpi-desync=fake --dpi-desync-repeats=11 --dpi-desync-fake-quic="/opt/zapret/quic_initial_www_google_com.bin" --new
--filter-udp=443 --dpi-desync=fake --dpi-desync-repeats=11 --new
--filter-tcp=80 --dpi-desync=fake,split2 --dpi-desync-autottl=2 --dpi-desync-fooling=md5sig --new
--filter-tcp=443 --hostlist="/opt/zapret/list-youtube.txt" --dpi-desync=fake,split2 --dpi-desync-repeats=11 --dpi-desync-fooling=md5sig --dpi-desync-fake-tls="/opt/zapret/tls_clienthello_www_google_com.bin" --new
--dpi-desync=fake,disorder2 --dpi-desync-autottl=2 --dpi-desync-fooling=md5sig
