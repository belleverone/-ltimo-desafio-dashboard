# -ltimo-desafio-dashboard
import pandas as pd

# Caminho do arquivo
file_path = "/mnt/data/0120950e-64c8-4092-a257-ba22ed198c69-2.xlsx"

# Lendo todas as planilhas do arquivo Excel
excel_file = pd.ExcelFile(file_path)
sheet_names = excel_file.sheet_names

# Visualizando as primeiras linhas de cada planilha para criar o read.me
sheet_previews = {sheet: excel_file.parse(sheet).head() for sheet in sheet_names}
sheet_previews.keys()
# Vamos dar uma olhada em cada uma das primeiras planilhas para entender seu conteúdo
assets_df = sheet_previews['A̳ssets']
bases_df = sheet_previews['B̳ases']
calculos_df = sheet_previews['C̳álculos']
dashboard_df = sheet_previews['D̳ashboard']

# Exibindo um resumo de cada planilha
assets_df.head(), bases_df.head(), calculos_df.head(), dashboard_df.head()
