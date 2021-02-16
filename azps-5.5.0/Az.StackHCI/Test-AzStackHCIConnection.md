---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 34831104bc1b27aa115d56545c784e0fea856ba4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178263"
---
# Test-AzStackHCIConnection

## SYNOPSIS
Test-AzStackHCIConnection verifica la connettività dai nodi cluster locali ai servizi di Azure richiesti da Azure Stack HCI.

## SINTASSI

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## DESCRIZIONE
Test-AzStackHCIConnection verifica la connettività dai nodi cluster locali ai servizi di Azure richiesti da Azure Stack HCI.

## ESEMPI

### ESEMPIO 1
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
Richiamo in uno dei nodi del cluster. Caso di esito positivo.

### ESEMPIO 2
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
Richiamo in uno dei nodi del cluster. Caso non riuscito.

## PARAMETERS

### -ComputerName
Specifica uno del nodo del cluster nel cluster locale che viene registrato in Azure.

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

### -Credential
Specifica le credenziali per NomeComputer.
Il valore predefinito è l'utente corrente che esegue il cmdlet.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Specifica l'ambiente di Azure.
Il valore predefinito è AzureCloud.
I valori validi sono AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -Area geografica
Specifica l'area geografica a cui connettersi.
Non usato a meno che non si tratta dell'area Canary.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

## OUTPUT

### PSCustomObject. Restituisce le proprietà seguenti in PSCustomObject
### Test: nome del test eseguito.
### EndpointTested: endpoint utilizzato nel test.
### IsRequired: True o False
### Risultato: Operazione riuscita o Non riuscita
### FailedNodes: elenco dei nodi in cui il test non è riuscito.
## NOTE

## COLLEGAMENTI CORRELATI
