---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurelocation
schema: 2.0.0
ms.openlocfilehash: 0d0f2856503943d19653dd09a8cb1c125fec9517
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030233"
---
# Get-AzsInfrastructureLocation

## Sinossi
Restituisce il percorso del tessuto richiesto.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Ottieni
```
Get-AzsInfrastructureLocation -FabricLocation <String> [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsInfrastructureLocation -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## Descrizione
Restituisce il percorso del tessuto richiesto.

## ESEMPI

### Esempio 1: 
```powershell
PS C:\> Get-AzsInfrastructureLocation

Return a list of all fabric locations.
```

Ottenere un elenco di tutte le posizioni in tessuto.

### Esempio 2: 
```powershell
PS C:\> Get-AzsInfrastructureLocation -Location "local"

Return a location based on the name.
```

Ottenere una posizione in base al nome.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### -FabricLocation
Posizione del tessuto.

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

### -Filtro
Parametro di filtro OData.

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -InputObject
Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -PassThru
Restituisce vero quando il comando riesce

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.
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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity

## OUTPUT

### Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IFabricLocation



## Note

Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.

INPUTOBJECT <IFabricAdminIdentity> : parametro Identity
  - `[Drive <String>]`: Nome dell'unità di archiviazione.
  - `[EdgeGateway <String>]`: Nome del gateway Edge.
  - `[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.
  - `[FabricLocation <String>]`: Posizione tessuto.
  - `[FileShare <String>]`: Nome condivisione file tessuto.
  - `[IPPool <String>]`: Nome pool IP.
  - `[Id <String>]`: Percorso identità risorse
  - `[InfraRole <String>]`: Nome ruolo infrastruttura.
  - `[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.
  - `[Location <String>]`: Posizione della risorsa.
  - `[LogicalNetwork <String>]`: Nome della rete logica.
  - `[LogicalSubnet <String>]`: Nome della subnet logica.
  - `[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.
  - `[Operation <String>]`: Identificatore operazione.
  - `[ResourceGroupName <String>]`: Nome del gruppo di risorse.
  - `[ScaleUnit <String>]`: Nome delle unità di scala.
  - `[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.
  - `[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.
  - `[StorageSubSystem <String>]`: Nome del sistema di archiviazione.
  - `[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.
  - `[Volume <String>]`: Nome del volume di archiviazione.

## COLLEGAMENTI CORRELATI

