---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374258"
---
# Test-AzStackHCIConnection

## Sinossi
Test-AzStackHCIConnection verifica la connettività dai nodi cluster locali ai servizi di Azure richiesti da Azure stack HCI.

## SINTASSI

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## Descrizione
Test-AzStackHCIConnection verifica la connettività dai nodi cluster locali ai servizi di Azure richiesti da Azure stack HCI.

## ESEMPI

### ESEMPIO 1
```
Invoking on one of the cluster node. Success case.
```

Test C:\PS \> -test di AzStackHCIConnection: connettersi al servizio EndpointTested di Azure stack HCI: https://azurestackhci-df.azurefd.net/health richiesto: risultato effettivo: riuscito

### ESEMPIO 2
```
Invoking on one of the cluster node. Failed case.
```

Test C:\PS \> -test di AzStackHCIConnection: connettersi al servizio di Azure stack HCI EndpointTested: https://azurestackhci-df.azurefd.net/health richiesto: risultato effettivo: errore FailedNodes: Node1inClus2, Node2inClus3

## PARAMETRI

### -Nomecomputer
Specifica uno dei nodi del cluster nel cluster locale che viene registrato in Azure.

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

### -Credenziale
Specifica le credenziali per nomecomputer.
Il valore predefinito è l'esecuzione del cmdlet da parte dell'utente corrente.

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
Specifica l'ambiente Azure.
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
Non usato a meno che non sia l'area Canarie.

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

## OUTPUT

### PSCustomObject. Restituisce le proprietà seguenti in PSCustomObject
### Test: nome del test eseguito.
### EndpointTested: endpoint usato nel test.
### Obbligatorio: vero o falso
### Risultato: riuscito o non riuscito
### FailedNodes: elenco dei nodi in cui il test non è riuscito.
## Note

## COLLEGAMENTI CORRELATI
