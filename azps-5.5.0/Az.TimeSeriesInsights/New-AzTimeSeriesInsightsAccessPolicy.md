---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197287"
---
# <span data-ttu-id="30ca3-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30ca3-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="30ca3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="30ca3-103">Creare o aggiornare i criteri di accesso nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="30ca3-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="30ca3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30ca3-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30ca3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="30ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="30ca3-106">Creare o aggiornare i criteri di accesso nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="30ca3-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="30ca3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30ca3-107">EXAMPLES</span></span>

### <span data-ttu-id="30ca3-108">Esempio 1: Creare criteri di accesso per un ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="30ca3-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="30ca3-109">Questo comando crea un criterio di accesso per un ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="30ca3-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="30ca3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30ca3-110">PARAMETERS</span></span>

### <span data-ttu-id="30ca3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ca3-111">-DefaultProfile</span></span>
<span data-ttu-id="30ca3-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30ca3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30ca3-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="30ca3-113">-Description</span></span>
<span data-ttu-id="30ca3-114">Descrizione dei criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="30ca3-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="30ca3-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="30ca3-115">-EnvironmentName</span></span>
<span data-ttu-id="30ca3-116">Nome dell'ambiente Time Series Insights associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="30ca3-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="30ca3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="30ca3-117">-Name</span></span>
<span data-ttu-id="30ca3-118">Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="30ca3-118">Name of the access policy.</span></span>

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

### <span data-ttu-id="30ca3-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="30ca3-119">-PrincipalObjectId</span></span>
<span data-ttu-id="30ca3-120">ObjectId dell'entità in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="30ca3-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="30ca3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30ca3-121">-ResourceGroupName</span></span>
<span data-ttu-id="30ca3-122">Nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="30ca3-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="30ca3-123">-Role</span><span class="sxs-lookup"><span data-stu-id="30ca3-123">-Role</span></span>
<span data-ttu-id="30ca3-124">Elenco dei ruoli assegnati all'entità nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="30ca3-124">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="30ca3-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30ca3-125">-SubscriptionId</span></span>
<span data-ttu-id="30ca3-126">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="30ca3-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="30ca3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30ca3-127">-Confirm</span></span>
<span data-ttu-id="30ca3-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30ca3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30ca3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30ca3-129">-WhatIf</span></span>
<span data-ttu-id="30ca3-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30ca3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30ca3-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30ca3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30ca3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ca3-132">CommonParameters</span></span>
<span data-ttu-id="30ca3-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30ca3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ca3-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30ca3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ca3-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="30ca3-135">INPUTS</span></span>

## <span data-ttu-id="30ca3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30ca3-136">OUTPUTS</span></span>

### <span data-ttu-id="30ca3-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="30ca3-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="30ca3-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="30ca3-138">NOTES</span></span>

<span data-ttu-id="30ca3-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="30ca3-139">ALIASES</span></span>

## <span data-ttu-id="30ca3-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30ca3-140">RELATED LINKS</span></span>

