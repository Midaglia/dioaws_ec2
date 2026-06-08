🚀 Sobre o Projeto
Este projeto consiste em uma solução automatizada de OCR (Reconhecimento Óptico de Caracteres) hospedada na nuvem AWS, projetada para transformar documentos estáticos em arquivos pesquisáveis de forma simples para o usuário final.

Como Funciona:
Entrada de Dados (Samba/SMB): O usuário simplesmente insere um arquivo PDF (não pesquisável) em uma pasta compartilhada na rede local, gerenciada pelo Samba e armazenada em um volume Amazon EBS.

Processamento (EC2 + Tesseract): Uma instância Amazon EC2 Linux Ubuntu — criada a partir de uma AMI (Amazon Machine Image) customizada com todas as dependências pré-instaladas — detecta o novo arquivo e aciona o Tesseract OCR.

Armazenamento Final (S3): Após o processamento, o arquivo convertido em PDF OCR (pesquisável) é enviado automaticamente para um bucket no Amazon S3, garantindo armazenamento seguro, durável e de longo prazo.

![Arquitetura do Projeto](image_7c435f.png)
