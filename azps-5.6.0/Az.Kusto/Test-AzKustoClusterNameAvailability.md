---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: dcc402b2db390403a6106953b3ecbdd6cc52a2b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954574"
---
# <span data-ttu-id="28f74-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="28f74-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="28f74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28f74-102">SYNOPSIS</span></span>
<span data-ttu-id="28f74-103">Verifica che il nome del cluster sia valido e non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="28f74-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="28f74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28f74-104">SYNTAX</span></span>

### <span data-ttu-id="28f74-105">CheckExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28f74-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="28f74-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="28f74-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="28f74-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="28f74-107">DESCRIPTION</span></span>
<span data-ttu-id="28f74-108">Verifica che il nome del cluster sia valido e non sia già in uso.</span><span class="sxs-lookup"><span data-stu-id="28f74-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="28f74-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28f74-109">EXAMPLES</span></span>

### <span data-ttu-id="28f74-110">Esempio 1: Verificare la disponibilità di un nome di cluster Kusto in uso</span><span class="sxs-lookup"><span data-stu-id="28f74-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="28f74-111">Il comando precedente restituisce se un cluster Kusto denominato "testnewkustocluster" si trova o meno nell'area "Stati Uniti orientali".</span><span class="sxs-lookup"><span data-stu-id="28f74-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="28f74-112">Esempio 2: Controllare la disponibilità di un nome di cluster Kusto che non è in uso</span><span class="sxs-lookup"><span data-stu-id="28f74-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="28f74-113">Il comando precedente restituisce se un cluster Kusto denominato "availablekustocluster" è presente nell'area "Stati Uniti orientali".</span><span class="sxs-lookup"><span data-stu-id="28f74-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="28f74-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28f74-114">PARAMETERS</span></span>

### <span data-ttu-id="28f74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f74-115">-DefaultProfile</span></span>
<span data-ttu-id="28f74-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28f74-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28f74-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28f74-117">-InputObject</span></span>
<span data-ttu-id="28f74-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="28f74-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28f74-119">-Location</span><span class="sxs-lookup"><span data-stu-id="28f74-119">-Location</span></span>
<span data-ttu-id="28f74-120">Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="28f74-120">Azure location.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f74-121">-Name</span><span class="sxs-lookup"><span data-stu-id="28f74-121">-Name</span></span>
<span data-ttu-id="28f74-122">Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="28f74-122">Cluster name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f74-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28f74-123">-SubscriptionId</span></span>
<span data-ttu-id="28f74-124">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="28f74-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="28f74-125">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="28f74-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f74-126">-Type</span><span class="sxs-lookup"><span data-stu-id="28f74-126">-Type</span></span>
<span data-ttu-id="28f74-127">Tipo di risorsa, Microsoft.Kusto/cluster.</span><span class="sxs-lookup"><span data-stu-id="28f74-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f74-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28f74-128">-Confirm</span></span>
<span data-ttu-id="28f74-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28f74-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f74-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28f74-130">-WhatIf</span></span>
<span data-ttu-id="28f74-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28f74-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28f74-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28f74-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f74-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f74-133">CommonParameters</span></span>
<span data-ttu-id="28f74-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28f74-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f74-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28f74-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f74-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="28f74-136">INPUTS</span></span>

### <span data-ttu-id="28f74-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="28f74-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="28f74-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28f74-138">OUTPUTS</span></span>

### <span data-ttu-id="28f74-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="28f74-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="28f74-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="28f74-140">NOTES</span></span>

<span data-ttu-id="28f74-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="28f74-141">ALIASES</span></span>

<span data-ttu-id="28f74-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="28f74-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="28f74-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="28f74-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="28f74-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="28f74-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="28f74-145">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="28f74-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="28f74-146">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="28f74-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="28f74-147">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="28f74-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="28f74-148">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="28f74-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="28f74-149">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="28f74-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="28f74-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="28f74-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="28f74-151">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="28f74-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="28f74-152">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="28f74-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="28f74-153">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="28f74-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="28f74-154">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="28f74-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="28f74-155">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="28f74-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="28f74-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28f74-156">RELATED LINKS</span></span>

