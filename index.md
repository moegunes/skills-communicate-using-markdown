# We add image now
![Image of Yaktocat](https://github.com/user-attachments/assets/644b962b-1ca5-4941-8ace-61f2cf1adb03)

``` python
def anal_chi0_thermo(rs,q):
    n0=(4*np.pi/3*rs**3)**(-1)
    kF=(3*np.pi**2*n0)**(1/3)

    filter_low=(q<1e-10)
    filter_high=(q>= 1e-10)
    q= q*filter_high +  1e-10*filter_low
    Q=q/(kF)
    res= -kF/(2*np.pi**2)* (1-(Q/4-1/Q)* np.log(np.abs((Q+2)/(Q-2))) )
    return res
```

then do

```
python3 -i run_script.py
```

## Todo list
- [x] Try the new proposition for the optimal alpha.
- [x] Do rs=2,5,10 full runs.
- [ ] Decide to keep alpha or do individual allpha opt for each vq,q.


