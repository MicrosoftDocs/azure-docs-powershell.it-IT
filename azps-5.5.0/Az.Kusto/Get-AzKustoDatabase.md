---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: a39578ffb7a0f3a5ecc6abc873f659b5d170aff5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185238"
---
# Get-AzKustoDatabase

## SYNOPSIS
Restituisce un database.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Ottieni
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIZIONE
Restituisce un database.

## ESEMPI

### Esempio 1: Elencare tutti i database Kusto in un cluster in base al nome
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

Il comando precedente restituisce tutti i database Kusto nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".

### Esempio 2: ottenere un database di Kusto specifico in base al nome
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

Il comando precedente restituisce il database Kusto denominato "mykustodatabase" nel cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg".

## PARAMETERS

### -ClusterName
Nome del cluster Kusto.

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

### -InputObject
Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Nome del database nel cluster Kusto.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse che contiene il cluster Kusto.

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

### -SubscriptionId
Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.
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

### Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity

## OUTPUT

### Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


INPUTOBJECT <IKustoIdentity> : parametro identity
  - `[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.
  - `[ClusterName <String>]`: nome del cluster Kusto.
  - `[DataConnectionName <String>]`: nome della connessione dati.
  - `[DatabaseName <String>]`: nome del database nel cluster Kusto.
  - `[Id <String>]`: percorso di identità della risorsa
  - `[Location <String>]`: posizione di Azure.
  - `[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.
  - `[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.
  - `[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.

## COLLEGAMENTI CORRELATI

