---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 20a9abc5cfc2ad2cc35bbedcf976daac286abb92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972397"
---
# <span data-ttu-id="a5138-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5138-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="a5138-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5138-102">SYNOPSIS</span></span>
<span data-ttu-id="a5138-103">Ottiene i criteri di accesso con il nome specificato nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a5138-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="a5138-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5138-104">SYNTAX</span></span>

### <span data-ttu-id="a5138-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5138-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a5138-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a5138-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a5138-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a5138-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5138-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a5138-108">DESCRIPTION</span></span>
<span data-ttu-id="a5138-109">Ottiene i criteri di accesso con il nome specificato nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a5138-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="a5138-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5138-110">EXAMPLES</span></span>

### <span data-ttu-id="a5138-111">Esempio 1: Elencare tutti i criteri di accesso in un ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="a5138-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="a5138-112">Questo comando elenca tutti i criteri di accesso in un ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a5138-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="a5138-113">Esempio 2: Ottenere un criterio di accesso specificato in base al nome</span><span class="sxs-lookup"><span data-stu-id="a5138-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="a5138-114">Questo comando ottiene un criterio di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="a5138-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="a5138-115">Esempio 3: Ottenere criteri di accesso specificati in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="a5138-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="a5138-116">Questo comando ottiene un criterio di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="a5138-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="a5138-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5138-117">PARAMETERS</span></span>

### <span data-ttu-id="a5138-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5138-118">-DefaultProfile</span></span>
<span data-ttu-id="a5138-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5138-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5138-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a5138-120">-EnvironmentName</span></span>
<span data-ttu-id="a5138-121">Nome dell'ambiente Time Series Insights associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a5138-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="a5138-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5138-122">-InputObject</span></span>
<span data-ttu-id="a5138-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a5138-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5138-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a5138-124">-Name</span></span>
<span data-ttu-id="a5138-125">Nome dei criteri di accesso Time Series Insights associati all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a5138-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5138-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5138-126">-ResourceGroupName</span></span>
<span data-ttu-id="a5138-127">Nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a5138-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a5138-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5138-128">-SubscriptionId</span></span>
<span data-ttu-id="a5138-129">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="a5138-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a5138-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5138-130">CommonParameters</span></span>
<span data-ttu-id="a5138-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5138-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5138-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5138-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5138-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="a5138-133">INPUTS</span></span>

### <span data-ttu-id="a5138-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a5138-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a5138-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5138-135">OUTPUTS</span></span>

### <span data-ttu-id="a5138-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="a5138-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="a5138-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="a5138-137">NOTES</span></span>

<span data-ttu-id="a5138-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a5138-138">ALIASES</span></span>

<span data-ttu-id="a5138-139">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a5138-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5138-140">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a5138-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5138-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a5138-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5138-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a5138-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a5138-143">`[AccessPolicyName <String>]`: nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="a5138-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a5138-144">`[EnvironmentName <String>]`: nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="a5138-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a5138-145">`[EventSourceName <String>]`: nome dell'origine evento Time Series Insights associata all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a5138-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a5138-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="a5138-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a5138-147">`[ReferenceDataSetName <String>]`: nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="a5138-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a5138-148">`[ResourceGroupName <String>]`: nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a5138-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a5138-149">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a5138-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a5138-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5138-150">RELATED LINKS</span></span>

