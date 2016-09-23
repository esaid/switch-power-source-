# ------------------------------------------------------------------
switch-power-source
# simulation LTspice  http://www.linear.com/designtools/software/#LTspice
# le montage permet de switcher automatiquement une tension entre 2 sources de tensions
 exemple : nous avons 2 sources de tensions avec :
V1 = 24v ou  12v ou  5v (3 tensions possibles)

V2 = 12v

Vout = soit V1 soit V2 si V2 > 4.6V ENVIRON  ,  1/((R6/R3+R6) / 0.6v pour le basculement du transistor Q2)

si V2 est defaillante alors Vout = V1

si on ne veut pas utiliser la source de tension V1 , alors il faut alimenter le montage par V2

la diode zener D3 permet de proteger le P - MOS , VGS =10V

D2 evite que la tension de 12v remonte dans V1 quand V1 = 5V

le transistor P-MOS IRF9Z34 (traditionnel) ou CMS pour des courants plus faible un cms ZXMP4A16G


