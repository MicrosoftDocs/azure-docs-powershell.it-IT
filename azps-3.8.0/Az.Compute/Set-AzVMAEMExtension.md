---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: b476254d5b9236aa95a30832499aca65a8a110c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019397"
---
# Set-AzVMAEMExtension

## Sinossi
Consente il supporto per il monitoraggio dei sistemi SAP.

## SINTASSI

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzVMAEMExtension** aggiorna la configurazione di una macchina virtuale per abilitare o aggiornare il supporto per il monitoraggio dei sistemi SAP installati nella macchina virtuale.
Il cmdlet installa l'estensione AEM (Azure Enhanced Monitoring) che raccoglie i dati sulle prestazioni e lo rende individuabile per il sistema SAP.

## ESEMPI

### Esempio 1: usare l'estensione AEM
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

Questo comando configura la macchina virtuale denominata Contoso-server per l'uso dell'estensione AEM.
Il comando specifica l'account di archiviazione denominato stdstorage.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWAD
Se questo parametro è disponibile, unifiedgroup consentirà la diagnostica di Windows Azure per questa macchina virtuale.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallNewExtension
Installare la nuova estensione VM per SAP.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NOWAIT
Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione. Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSType
Specifica il tipo di sistema operativo del disco del sistema operativo.
Se il disco del sistema operativo non ha un tipo, è necessario specificare questo parametro.
I valori accettabili per questo parametro sono: Windows e Linux.

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SetAccessToIndividualResources
Imposta l'accesso dell'identità VM alle singole risorse, ad esempio i dischi di dati anziché il gruppo di risorse completo.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipStorage
Indica che questo cmdlet ignora la configurazione dello spazio di archiviazione.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse

## Note

## COLLEGAMENTI CORRELATI

[Get-AzVMAEMExtension](./Get-AzVMAEMExtension.md)

[Remove-AzVMAEMExtension](./Remove-AzVMAEMExtension.md)

[Test-AzVMAEMExtension](./Test-AzVMAEMExtension.md)


