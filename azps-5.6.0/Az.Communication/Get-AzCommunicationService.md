---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: f9f4cc86a07c50718511c3ed0889d96f7acec9a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991673"
---
# Get-AzCommunicationService

## SYNOPSIS
Ottenere CommunicationService e le relative proprietà.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Ottieni
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Elenco1
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIZIONE
Ottenere CommunicationService e le relative proprietà.

## ESEMPI

### Esempio 1: Elencare i servizi di comunicazione esistenti per una sottoscrizione
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

Restituisce un elenco di tutte le risorse ACS nell'abbonamento.

### Esempio 2: Ottenere informazioni sulla risorsa di comunicazione di Azure specificata
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

Restituisce le informazioni su una risorsa ACS, se viene trovato un parametro fornito corrispondente.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Nome della risorsa CommunicationService.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse che contiene la risorsa.
È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.
L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity

## OUTPUT

### Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


INPUTOBJECT <ICommunicationIdentity> : parametro Identity
  - `[CommunicationServiceName <String>]`: nome della risorsa CommunicationService.
  - `[Id <String>]`: percorso di identità della risorsa
  - `[Location <String>]`: l'area geografica Azure
  - `[OperationId <String>]`: ID di un'operazione di sincronizzazione in corso
  - `[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.
  - `[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.

## COLLEGAMENTI CORRELATI

