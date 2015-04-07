def GPS():
    print 'Digite as coordenadas geograficas x, y e z'
    x=float(raw_input())
    y=float(raw_input())
    z=float(raw_input())
    a=6378160
    e=0.00669454185
    lamb= math.atan2(y,x)
    p=math.sqrt(math.fabs(math.pow(x,2)+math.pow(y,2)))
    h=0
    n=1
    oi=z/(p*(1-e*n/(n+h)))
    teta=math.atan(oi)
    for i in range(1,5):
        n=float(a)/math.sqrt(1-e*math.pow(math.sin(teta),2))
        h=float(p)/math.cos(teta)-n
        oi=float(z)/(p*(1-e*n/(n+h)))
        teta=math.atan(oi)
    ra=math.degrees(teta)
    rb=math.degrees(lamb)
    print 'Latitude: ',rb,' graus'
    print 'Longitude: ',ra,' graus'
    print 'Altitude: ',1000*h,'m'
