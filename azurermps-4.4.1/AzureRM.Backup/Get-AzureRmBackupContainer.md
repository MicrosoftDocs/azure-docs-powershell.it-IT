---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: c7bcddca0cfef631f7501dfb6c017f2c6ef7af25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685695"
---
# Get-AzureRmBackupContainer

## Sinossi
Ottiene i contenitori di backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmBackupContainer** ottiene i contenitori di backup di Azure.

Un **AzureBackupContainer** incapsula origini dati, elementi protetti e punti di ripristino.
Un **AzureBackupContainer** può essere uno dei seguenti: 

- Un computer Windows Server
- Un server SCDPM (System Center Data Protection Manager) 
- Macchina virtuale di una infrastruttura Azure come servizio (IaaS)

Prima di poter eseguire il backup di un'origine dati o di un elemento, è necessario registrare il contenitore che lo contiene con il servizio di backup di Azure.
Il contenitore deve essere autenticato per inviare dati di backup al Vault di backup.
Per i computer Windows Server e i server SCDPM, la registrazione viene mantenuta con il nome di dominio completo del server.

## ESEMPI

### Esempio 1: visualizzare tutti i server registrati in un Vault
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .
Il comando Archivia l'oggetto nella variabile $Vault.

Il secondo comando consente di ottenere tutti i contenitori di tipo Windows dal Vault in $Vault.

### Esempio 2: ottenere un contenitore specifico
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

Questo comando ottiene il contenitore denominato DPMSERVER. CONTOSO.COM.
Il comando specifica il Vault in $Vault e il tipo di contenitore.

### Esempio 3: visualizzare tutte le macchine virtuali di Azure registrate
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

Questo comando consente di ottenere le macchine virtuali registrate dal Vault in $Vault.

## PARAMETRI

### -ManagedResourceGroupName
Specifica il nome del gruppo di risorse associato al contenitore.
Questo nome è lo stesso valore specificato per il parametro *ServiceName* o *ResourceGroupName* del cmdlet Register-AzureRmBackupContainer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome del contenitore ottenuto da questo cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Stato
Specifica lo stato corrente dei contenitori ottenuti da questo cmdlet.
I valori accettabili per questo parametro sono i seguenti:

- NotRegistered 
- Registrato 
- Registrazione

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digitare
Specifica il tipo di contenitori ottenuti da questo cmdlet.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Specifica un archivio di backup da cui questo cmdlet ottiene i contenitori.
Per ottenere un **AzureRmBackupVault** , usare il cmdlet Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### AzureBackupVault

## OUTPUT

### AzureBackupContainer

## Note
* Nessuno

## COLLEGAMENTI CORRELATI

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Registro-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)

[Annullamento della registrazione-AzureRmBackupContainer](./Unregister-AzureRmBackupContainer.md)


