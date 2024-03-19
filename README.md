##ARMAZENANDO DADOS

projeto = input("Digite a descriçao do projeto: ")

estimativa = input("Digite as Horas estimadas: ")

valor_hora = input("Digite o Valor da hora trabahada: ")

prazo_entrega = input("Digite o Prazo da entrega: ")

##GERANDO PDF

from fpdf import FPDF

pdf = FPDF()

pdf.add_page()
pdf.set_font("Arial")
pdf.image("02.png", x=0, y=0)

pdf.text(28, 137, projeto)
pdf.text(102, 137, (estimativa) + (hora))
pdf.text(170, 137, (valor_hora) + (real) + (hora))
pdf.text(115, 137, prazo_entrega)

pdf.text(139, 172.7, str(valor_total) + (real))



pdf.output("prj1.pdf")

print("Orcamento gerado com sucesso")

##REALIZANDO CALCULOS

valor_total = int(estimativa) * int(valor_hora)
