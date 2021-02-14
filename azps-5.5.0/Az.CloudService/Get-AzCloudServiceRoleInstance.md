---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 55416adbd2ffbcb816e5652ad33e1777594fdcb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181799"
---
# Get-AzCloudServiceRoleInstance

## SYNOPSIS
Ottiene un'istanza del ruolo da un servizio cloud.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Ottieni
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIZIONE
Ottiene un'istanza del ruolo da un servizio cloud.

## ESEMPI

### Esempio 1: Ottenere tutte le istanze di ruolo
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard
ContosoFrontEnd_IN_1    eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard

```

Questo comando ottiene le proprietà di tutte le istanze di ruoli del servizio cloud denominate ContosoCS che appartengono al gruppo di risorse denominato ContosOrg.

### Esempio 2: Ottenere le proprietà per una singola istanza del ruolo
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard

```

Questo comando recupera le proprietà dell'istanza del ruolo ContosoFrontEnd_IN_0 servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.

## PARAMETERS

### -CloudServiceName
.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Expand
Espressione di espansione da applicare all'operazione.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.InstanceViewTypes
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleInstanceName
Nome dell'istanza del ruolo.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.
L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.

```yaml
Type: System.String[]
Parameter Sets: Get, List
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

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity

## OUTPUT

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


INPUTOBJECT <ICloudServiceIdentity> : parametro identity
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`: percorso di identità della risorsa
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`: nome dell'istanza del ruolo.
  - `[RoleName <String>]`: nome del ruolo.
  - `[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.
  - `[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento. I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.

## COLLEGAMENTI CORRELATI

