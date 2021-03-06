## Transfer protocol over UDP

QUIC is a transfer protocol implemented in user-space on top of UDP. If you
watch your network traffic casually, you will see QUIC appear as UDP packets.

HTTP-over-QUIC will default to using UDP port 443.

## Will it work?

There are enterprises and other network setups that block UDP traffic on other
ports than 53 (used for DNS). Others throttle such data in ways that makes
QUIC perform worse than TCP based protocols. There's no end to what some
operators may do.

For the foreseeable future, all use of QUIC-based transports will probably
have to be able to gracefully fall-back to another (TCP-based)
alternative. Google engineers have previously mentioned measured failure rates
in the low single-digit percentages.

## Will it improve?

Chances are that if QUIC proves to be a valuable addition to the Internet
world, people will want to use it and they will want it to function in their
networks and then companies may start to reconsider their obstacles. During
the years the development of QUIC has progressed, the success rate across the
Internet has increased.
