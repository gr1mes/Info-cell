
BLACK = '\033[30m'
RED = '\033[31m'
GREEN = '\033[32m'
YELLOW = '\033[33m'
BLUE = '\033[34m'
MAGENTA = '\033[35m'
CYAN = '\033[36m'
WHITE = '\033[37m'
RESET = '\033[39m'
print(RED+"
print("                  .88888888:.
print("                88888888.88888.
print("              .8888888888888888.
print("              888888888888888888
print("              88' _`88'_  `88888
print("              88 88 88 88  88888
print("              88_88_::_88_:88888
print("              88:::,::,:::::8888
print("              88`:::::::::'`8888
print("             .88  `::::'    8:88.
print("            8888            `8:888.
print("          .8888'             `888888.
print("         .8888:..  .::.  ...:'8888888:.
print("        .8888.'     :'     `'::`88:88888
print("       .8888        '         `.888:8888.
print("      888:8         .           888:88888
print("    .888:88        .:           888:88888:
print("    8888888.       ::           88:888888
print("    `.::.888.      ::          .88888888
print("   .::::::.888.    ::         :::`8888'.:.
print("  ::::::::::.888   '         .::::::::::::
print("  ::::::::::::.8    '      .:8::::::::::::.
print(" .::::::::::::::.        .:888:::::::::::::
print(" :::::::::::::::88:.__..:88888:::::::::::'
print("  `'.:::::::::::88888888888.88:::::::::'
print("     `':::_:' -- '' -'-' `':_::::'`
print("\033[33m--------------------------------------")
print(RED+"Autor    : GRIMES")
print("TIK TOK  : grimess.cd")
print("-------------------------------------- \n")
print(RED+"escribe el numero de telefono junto\ncon el prefijo, ejemplo: +541139893241\n")

api_key = '48d04397c36551c48eced6a4304b66f6'

number = int(input(RED+"Numero de telefono: "+RESET))

data = requests.get("http://apilayer.net/api/validate?access_key=%s&number=%s&country_code&format=1" % (api_key, number))

for key, value in data.json().items():

    print("%s: %s" % (key, value))
