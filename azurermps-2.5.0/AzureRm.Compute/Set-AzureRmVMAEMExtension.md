---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: 01eb8cba77177ca35f2e1b73ec410baa44e4a58c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865931"
---
# Set-AzureRmVMAEMExtension

## Sinossi
Consente il supporto per il monitoraggio dei sistemi SAP.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmVMAEMExtension** aggiorna la configurazione di una macchina virtuale per abilitare o aggiornare il supporto per il monitoraggio dei sistemi SAP installati nella macchina virtuale.
Il cmdlet installa l'estensione AEM (Azure Enhanced Monitoring) che raccoglie i dati sulle prestazioni e lo rende individuabile per il sistema SAP.

## ESEMPI

### Esempio 1: usare l'estensione AEM
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

Questo comando configura la macchina virtuale denominata Contoso-server per l'uso dell'estensione AEM.
Il comando specifica l'account di archiviazione denominato stdstorage.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWAD
Indica che questo cmdlet non Abilita la diagnostica Azure per la macchina virtuale.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWAD
Se questo parametro è disponibile, unifiedgroup consentirà la diagnostica di Windows Azure per questa macchina virtuale.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSType
Specifica il tipo di sistema operativo del disco del sistema operativo.
Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.
I valori accettabili per questo parametro sono: Windows e Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse della macchina virtuale modificato da questo cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipStorage
Indica che questo cmdlet ignora la configurazione dello spazio di archiviazione.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Specifica il nome di una macchina virtuale.
Questo cmdlet aggiunge l'estensione AEM per la macchina virtuale specificata da questo parametro.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WADStorageAccountName
Specifica il nome dell'account di archiviazione usato da questo cmdlet per configurare l'estensione LinuxDiagnostics o IaaSDiagnostics.
Se la macchina virtuale non usa un account di archiviazione standard, devi specificare un valore per questo parametro.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmVMAEMExtension](./Get-AzureRmVMAEMExtension.md)

[Remove-AzureRmVMAEMExtension](./Remove-AzureRmVMAEMExtension.md)

[Test-AzureRmVMAEMExtension](./Test-AzureRmVMAEMExtension.md)


