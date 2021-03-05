---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 9a57b38f77d299a69cbb1f38b006d616b9c9b825
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981373"
---
# <span data-ttu-id="24677-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24677-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="24677-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24677-102">SYNOPSIS</span></span>
<span data-ttu-id="24677-103">Creare o aggiornare i criteri di accesso nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="24677-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="24677-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24677-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="24677-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="24677-105">DESCRIPTION</span></span>
<span data-ttu-id="24677-106">Creare o aggiornare i criteri di accesso nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="24677-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="24677-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24677-107">EXAMPLES</span></span>

### <span data-ttu-id="24677-108">Esempio 1: Creare criteri di accesso per un ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="24677-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="24677-109">Questo comando crea un criterio di accesso per un ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="24677-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="24677-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24677-110">PARAMETERS</span></span>

### <span data-ttu-id="24677-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24677-111">-DefaultProfile</span></span>
<span data-ttu-id="24677-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24677-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24677-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="24677-113">-Description</span></span>
<span data-ttu-id="24677-114">Descrizione dei criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="24677-114">An description of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24677-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="24677-115">-EnvironmentName</span></span>
<span data-ttu-id="24677-116">Nome dell'ambiente Approfondimenti serie temporale associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="24677-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="24677-117">-Name</span><span class="sxs-lookup"><span data-stu-id="24677-117">-Name</span></span>
<span data-ttu-id="24677-118">Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="24677-118">Name of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24677-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="24677-119">-PrincipalObjectId</span></span>
<span data-ttu-id="24677-120">ObjectId dell'entità in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24677-120">The objectId of the principal in Azure Active Directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24677-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24677-121">-ResourceGroupName</span></span>
<span data-ttu-id="24677-122">Nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="24677-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="24677-123">-Role</span><span class="sxs-lookup"><span data-stu-id="24677-123">-Role</span></span>
<span data-ttu-id="24677-124">Elenco dei ruoli assegnati all'entità nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="24677-124">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24677-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24677-125">-SubscriptionId</span></span>
<span data-ttu-id="24677-126">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="24677-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24677-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24677-127">-Confirm</span></span>
<span data-ttu-id="24677-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24677-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24677-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24677-129">-WhatIf</span></span>
<span data-ttu-id="24677-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24677-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24677-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24677-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24677-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24677-132">CommonParameters</span></span>
<span data-ttu-id="24677-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24677-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24677-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="24677-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24677-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="24677-135">INPUTS</span></span>

## <span data-ttu-id="24677-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24677-136">OUTPUTS</span></span>

### <span data-ttu-id="24677-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="24677-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="24677-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="24677-138">NOTES</span></span>

<span data-ttu-id="24677-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="24677-139">ALIASES</span></span>

## <span data-ttu-id="24677-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24677-140">RELATED LINKS</span></span>

