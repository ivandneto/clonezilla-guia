# Parte 1 — Introdução ao Clonezilla

O **Clonezilla** é uma poderosa ferramenta open source utilizada para clonar discos, clonar partições e gerar imagens completas de sistemas operacionais, possibilitando sua restauração em caso de falhas ou migração para novos dispositivos. Mesmo possuindo interface simples e textual, é extremamente robusto e flexível.

Este documento faz parte do **Guia Clonezilla — Parte 1**, contendo todos os procedimentos para:

- Clonar discos  
- Clonar partições  
- Criar backups locais  
- Criar backups remotos via SSH  
- Criar backups via Samba  
- Restaurar imagens (local, SSH e Samba)  

---

## 🔹 Clonezilla Live vs Clonezilla SE

O projeto disponibiliza **duas variantes**:

### **1) Clonezilla Live**
- Distribuição live (CD/USB)  
- Opera em modo **unicast**  
- Excelente para clonar máquinas individuais  
- Pode clonar diretamente disco→disco sem salvar imagem  

### **2) Clonezilla SE (Server Edition)**
- Permite operações em:
  - **Unicast**
  - **Multicast**
  - **Broadcast**
- Clonagem simultânea de múltiplas máquinas
- Ideal para redes corporativas e laboratórios

📌 *Esta Parte 1 aborda apenas o Clonezilla Live.*

---

## 🔹 Principais Características

1. Licença **GPL**
2. Suporte aos principais sistemas de arquivos:
   - ext2/ext3/ext4  
   - ReiserFS/Reiser4  
   - XFS / JFS  
   - btrfs  
   - FAT/NTFS  
   - HFS, UFS  
   - VMFS3/VMFS5 (VMware)
3. Funciona com Linux, Windows, macOS, BSD (32 e 64 bits)
4. Copia apenas blocos utilizados (backup eficiente)
5. Suporte a **LVM2**
6. Pode restaurar imagem para múltiplos dispositivos (SE)
7. Suporte a multicast para grandes implantações (SE)

---

## 🔹 Limitações Importantes

1. O **destino deve ter tamanho igual ou maior** que a origem  
2. **Não suporta backup incremental/diferencial**  
3. Dispositivo de origem precisa estar **offline**  
4. Restauração também exige destino **offline**  
5. Não permite navegar dentro da imagem sem ferramentas extras  
6. **RAID por software não suportado** no momento  
7. Após restaurar, pode ser necessário **redimensionamento manual** em alguns casos

---

## 🔹 Uso combinado com Parted Magic

Este guia utiliza o **Parted Magic**, pois ele:

- Inclui Clonezilla + GParted  
- Facilita redimensionamento de partições  
- Excelente para casos onde o disco de destino é maior

Baixe em:  
https://partedmagic.com/

Caso deseje usar apenas Clonezilla Live:  
https://clonezilla.org/downloads

---

## 🔹 Organização das Páginas

- **Página 1:** Introdução  
- **Página 2:** Clonagem de dispositivos  
- **Página 3:** Backup local  
- **Página 4:** Restauração local  
- **Página 5:** Backup via SSH  
- **Página 6:** Restauração via SSH  
- **Página 7:** Backup via Samba  
- **Página 8:** Restauração via Samba  
- **Página 9:** Conclusão  

---

➡ **[Próxima Página → Clonagem de Dispositivos](pagina-2.md)**  
