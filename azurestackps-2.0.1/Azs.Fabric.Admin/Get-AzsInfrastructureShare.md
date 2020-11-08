---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureshare
schema: 2.0.0
ms.openlocfilehash: e5fce1490b27bb569ce493a66a1c2646b73466a4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023278"
---
# Get-AzsInfrastructureShare

## Sinossi
Restituisce la condivisione file in tessuto richiesto.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### Ottieni
```
Get-AzsInfrastructureShare -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsInfrastructureShare -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## Descrizione
Restituisce la condivisione file in tessuto richiesto.

## ESEMPI

### Esempio 1:
```powershell
PS C:\> Get-AzsInfrastructureShare
```

Restituisce un elenco di tutte le condivisioni file.

### Esempio 2:
```powershell
PS C:\> Get-AzsInfrastructureShare -Name SU1_ObjStore_1
```

Restituisce una condivisione di file in base al nome.

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

### -Posizione
Posizione della risorsa.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Nome
Nome condivisione file in tessuto.

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

### -PassThru
Restituisce vero quando il comando riesce

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

### -Skip
Parametro OData skip.

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

### -Inizio pagina
Parametro OData superiore.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity

## OUTPUT

### Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IFileShare



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

