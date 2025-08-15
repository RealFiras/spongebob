SpongeBob Crypto TCP (Railway)
محلياً
اختياري: جرّب socat محلياً بنفس الفكرة
لازم يكون socat مثبت عندك
export PORT=9000 socat TCP-LISTEN:$PORT,fork,reuseaddr EXEC:"python Spongebob.py",pty,setsid,ctty

افتح اتصال:
nc 127.0.0.1 9001

على Railway
ادفع الريبو إلى GitHub.
من Railway: New Project → Deploy from GitHub.
بعد الديبولوي، فعّل TCP Proxy من: Service → Settings → Networking → TCP Proxy (اختَر البورت الداخلي = $PORT).
اختبر: nc <TCP_HOST> <TCP_PORT>