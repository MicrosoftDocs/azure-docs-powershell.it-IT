---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: fc4d1edfe23e6520af230960b6a9262afba43b6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964558"
---
# <span data-ttu-id="7084f-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="7084f-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="7084f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7084f-102">SYNOPSIS</span></span>
<span data-ttu-id="7084f-103">Restituisce una configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="7084f-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="7084f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7084f-104">SYNTAX</span></span>

### <span data-ttu-id="7084f-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7084f-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7084f-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="7084f-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7084f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7084f-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7084f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7084f-108">DESCRIPTION</span></span>
<span data-ttu-id="7084f-109">Restituisce una configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="7084f-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="7084f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7084f-110">EXAMPLES</span></span>

### <span data-ttu-id="7084f-111">Esempio 1: Elencare tutte le configurazioni di database collegate in un cluster</span><span class="sxs-lookup"><span data-stu-id="7084f-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="7084f-112">Il comando precedente elenca tutte le ConfigurazioniDatabase Allegate nel cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="7084f-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="7084f-113">Esempio 2: Ottenere una specifica AttachedDatabaseConfiguration in un cluster</span><span class="sxs-lookup"><span data-stu-id="7084f-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="7084f-114">Il comando precedente restituisce le ConfigurazioniDatabase Allegate denominate "myfollowerconfiguration" nel cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="7084f-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="7084f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7084f-115">PARAMETERS</span></span>

### <span data-ttu-id="7084f-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7084f-116">-ClusterName</span></span>
<span data-ttu-id="7084f-117">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7084f-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7084f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7084f-118">-DefaultProfile</span></span>
<span data-ttu-id="7084f-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7084f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7084f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7084f-120">-InputObject</span></span>
<span data-ttu-id="7084f-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7084f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7084f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7084f-122">-Name</span></span>
<span data-ttu-id="7084f-123">Nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="7084f-123">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7084f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7084f-124">-ResourceGroupName</span></span>
<span data-ttu-id="7084f-125">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7084f-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7084f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7084f-126">-SubscriptionId</span></span>
<span data-ttu-id="7084f-127">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7084f-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7084f-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7084f-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7084f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7084f-129">CommonParameters</span></span>
<span data-ttu-id="7084f-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7084f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7084f-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7084f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7084f-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="7084f-132">INPUTS</span></span>

### <span data-ttu-id="7084f-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7084f-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7084f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7084f-134">OUTPUTS</span></span>

### <span data-ttu-id="7084f-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="7084f-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="7084f-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="7084f-136">NOTES</span></span>

<span data-ttu-id="7084f-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7084f-137">ALIASES</span></span>

<span data-ttu-id="7084f-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="7084f-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7084f-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7084f-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7084f-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7084f-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7084f-141">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="7084f-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7084f-142">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="7084f-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7084f-143">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7084f-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7084f-144">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="7084f-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7084f-145">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7084f-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7084f-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="7084f-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7084f-147">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7084f-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7084f-148">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="7084f-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7084f-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7084f-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7084f-150">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7084f-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7084f-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7084f-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7084f-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7084f-152">RELATED LINKS</span></span>

