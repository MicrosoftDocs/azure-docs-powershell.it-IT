---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: fd735b1d343c046f9ca2f0528bff4bf7ce8a403d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361591"
---
# <span data-ttu-id="f9f93-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9f93-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="f9f93-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9f93-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f93-103">Restituisce la configurazione di un database allegato.</span><span class="sxs-lookup"><span data-stu-id="f9f93-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="f9f93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9f93-104">SYNTAX</span></span>

### <span data-ttu-id="f9f93-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9f93-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f9f93-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f9f93-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f9f93-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f9f93-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9f93-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9f93-108">DESCRIPTION</span></span>
<span data-ttu-id="f9f93-109">Restituisce la configurazione di un database allegato.</span><span class="sxs-lookup"><span data-stu-id="f9f93-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="f9f93-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9f93-110">EXAMPLES</span></span>

### <span data-ttu-id="f9f93-111">Esempio 1: elencare tutte le AttachedDatabaseConfigurations in un cluster</span><span class="sxs-lookup"><span data-stu-id="f9f93-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="f9f93-112">Il comando precedente elenca tutti i AttachedDatabaseConfigurations nel cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="f9f93-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="f9f93-113">Esempio 2: ottenere un AttachedDatabaseConfiguration specifico in un cluster</span><span class="sxs-lookup"><span data-stu-id="f9f93-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="f9f93-114">Il comando precedente restituisce il AttachedDatabaseConfigurations denominato "myfollowerconfiguration" nel cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="f9f93-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="f9f93-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9f93-115">PARAMETERS</span></span>

### <span data-ttu-id="f9f93-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f9f93-116">-ClusterName</span></span>
<span data-ttu-id="f9f93-117">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="f9f93-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f9f93-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f93-118">-DefaultProfile</span></span>
<span data-ttu-id="f9f93-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9f93-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9f93-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9f93-120">-InputObject</span></span>
<span data-ttu-id="f9f93-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f9f93-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f9f93-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9f93-122">-Name</span></span>
<span data-ttu-id="f9f93-123">Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="f9f93-123">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="f9f93-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f93-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9f93-125">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="f9f93-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f9f93-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9f93-126">-SubscriptionId</span></span>
<span data-ttu-id="f9f93-127">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f9f93-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f9f93-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f9f93-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f9f93-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f93-129">CommonParameters</span></span>
<span data-ttu-id="f9f93-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9f93-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f93-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9f93-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f93-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9f93-132">INPUTS</span></span>

### <span data-ttu-id="f9f93-133">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f9f93-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f9f93-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9f93-134">OUTPUTS</span></span>

### <span data-ttu-id="f9f93-135">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9f93-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="f9f93-136">Note</span><span class="sxs-lookup"><span data-stu-id="f9f93-136">NOTES</span></span>

<span data-ttu-id="f9f93-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f9f93-137">ALIASES</span></span>

<span data-ttu-id="f9f93-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9f93-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f9f93-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f9f93-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f9f93-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f9f93-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f9f93-141">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f9f93-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f9f93-142">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="f9f93-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f9f93-143">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="f9f93-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f9f93-144">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="f9f93-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f9f93-145">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="f9f93-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f9f93-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="f9f93-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f9f93-147">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f9f93-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f9f93-148">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="f9f93-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f9f93-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="f9f93-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f9f93-150">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f9f93-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f9f93-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f9f93-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f9f93-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9f93-152">RELATED LINKS</span></span>

