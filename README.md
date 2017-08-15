# ____________________teste
calculadora


class Teste(object):


	variavel_temp_dado = list()

	def supervisor(self):

		vali = {'novo_pedido': False, 'armazenamento': False}  # Controla o recebimento de novos produtos e sua entrega
		ver = {'s':self.encarregado,'S':self.encarregado,'N': False,'n': False}

		for x, y in vali.items():
			if x == 'novo_pedido':
				print(self.mensagem(7))
				self.encarregado()
				resp = input(self.mensagem(5))  # --- > S ou N
				while ver.get(resp):
					print('Dentro do While')
					break
			elif x == 'armazenamento':
				print('Esta na segunda etapa de armazenamento')


	def encarregado(self): # criar um novo produto / pega os dados e cria o objeto

		{'nome': None, 'valor_total': None, 'peso_bruto': None, 'qtd_utl': None, 'percent_utl': None,
		 'valor_percent': None}
		self.valid = {1: False, 2: False, 3: False, 4: False}  # Roteiro para entrada do produto
		for x,y in self.valid.items():
			while (y == False):
				if self.valida(x):
					self.valid[x] = True
					break
				else:
					continue
		return True


	def mensagem(self,a):
		mens = a
		infor = {
			1: "Informe o nome da produto: ",
			2: "Informe o valor do produto: R$ ",
			3: "Informe o peso total descrito na embalagem do produto: ",
			4: "Informe a quantidade utilizada na receita (ex. 150mg) ou (ex. 50ml): ",
			5: "Deseja adicionar outro ingrediente? (S)im ou (N)ão: ",
			6: "Dados informados incorretos! ",
			7: "Informe os ingredientes e seus dados."
			}
		return infor[mens]


	def entrada(self,a): #1 - nome 2 - sobrenome

		info_msg = a
		dados = input(self.mensagem(info_msg))
		return dados

	def valida(self,a):
		temp_dad = a
		temp = self.entrada(temp_dad)
		if (temp != ''):
			self.variavel_temp_dado.append(temp)
			return True
		else:
			return False

	def armazena(self,a):
		base = {'nome':None,'valor_total':None,'peso_bruto':None,'qtd_utl':None,'percent_utl':None,'valor_percent':None}


ft = Teste()
ff = ft.supervisor()
