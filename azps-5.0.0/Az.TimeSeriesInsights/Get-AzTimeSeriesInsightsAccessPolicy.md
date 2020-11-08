---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200058"
---
# <span data-ttu-id="6a5b5-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6a5b5-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="6a5b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a5b5-102">SYNOPSIS</span></span>
<span data-ttu-id="6a5b5-103">Ottiene i criteri di accesso con il nome specificato nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="6a5b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a5b5-104">SYNTAX</span></span>

### <span data-ttu-id="6a5b5-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a5b5-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6a5b5-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="6a5b5-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6a5b5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6a5b5-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a5b5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a5b5-108">DESCRIPTION</span></span>
<span data-ttu-id="6a5b5-109">Ottiene i criteri di accesso con il nome specificato nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="6a5b5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a5b5-110">EXAMPLES</span></span>

### <span data-ttu-id="6a5b5-111">Esempio 1: elenca tutti i criteri di accesso in un ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="6a5b5-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="6a5b5-112">Questo comando elenca tutti i criteri di accesso in un ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="6a5b5-113">Esempio 2: ottenere un criterio di accesso specificato per nome</span><span class="sxs-lookup"><span data-stu-id="6a5b5-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="6a5b5-114">Questo comando ottiene un criterio di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="6a5b5-115">Esempio 3: ottenere un criterio di accesso specificato per oggetto</span><span class="sxs-lookup"><span data-stu-id="6a5b5-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="6a5b5-116">Questo comando ottiene un criterio di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="6a5b5-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a5b5-117">PARAMETERS</span></span>

### <span data-ttu-id="6a5b5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a5b5-118">-DefaultProfile</span></span>
<span data-ttu-id="6a5b5-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a5b5-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="6a5b5-120">-EnvironmentName</span></span>
<span data-ttu-id="6a5b5-121">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="6a5b5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a5b5-122">-InputObject</span></span>
<span data-ttu-id="6a5b5-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a5b5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a5b5-124">-Name</span></span>
<span data-ttu-id="6a5b5-125">Il nome della serie temporale approfondisce i criteri di accesso associati all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="6a5b5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a5b5-126">-ResourceGroupName</span></span>
<span data-ttu-id="6a5b5-127">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="6a5b5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a5b5-128">-SubscriptionId</span></span>
<span data-ttu-id="6a5b5-129">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6a5b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a5b5-130">CommonParameters</span></span>
<span data-ttu-id="6a5b5-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a5b5-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a5b5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a5b5-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a5b5-133">INPUTS</span></span>

### <span data-ttu-id="6a5b5-134">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="6a5b5-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="6a5b5-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a5b5-135">OUTPUTS</span></span>

### <span data-ttu-id="6a5b5-136">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="6a5b5-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="6a5b5-137">Note</span><span class="sxs-lookup"><span data-stu-id="6a5b5-137">NOTES</span></span>

<span data-ttu-id="6a5b5-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6a5b5-138">ALIASES</span></span>

<span data-ttu-id="6a5b5-139">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a5b5-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a5b5-140">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a5b5-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a5b5-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="6a5b5-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a5b5-143">`[AccessPolicyName <String>]`: Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="6a5b5-144">`[EnvironmentName <String>]`: Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="6a5b5-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="6a5b5-145">`[EventSourceName <String>]`: Il nome dell'origine dell'evento Insights serie temporali associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="6a5b5-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="6a5b5-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a5b5-147">`[ReferenceDataSetName <String>]`: Nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="6a5b5-148">`[ResourceGroupName <String>]`: Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="6a5b5-149">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="6a5b5-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a5b5-150">RELATED LINKS</span></span>
