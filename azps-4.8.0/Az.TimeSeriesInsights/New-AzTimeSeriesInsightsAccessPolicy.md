---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191402"
---
# <span data-ttu-id="aa48e-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa48e-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="aa48e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa48e-102">SYNOPSIS</span></span>
<span data-ttu-id="aa48e-103">Creare o aggiornare un criterio di accesso nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="aa48e-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="aa48e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa48e-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aa48e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa48e-105">DESCRIPTION</span></span>
<span data-ttu-id="aa48e-106">Creare o aggiornare un criterio di accesso nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="aa48e-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="aa48e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa48e-107">EXAMPLES</span></span>

### <span data-ttu-id="aa48e-108">Esempio 1: creare un criterio di accesso per un ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="aa48e-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="aa48e-109">Questo comando crea un criterio di accesso per un ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="aa48e-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="aa48e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa48e-110">PARAMETERS</span></span>

### <span data-ttu-id="aa48e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa48e-111">-DefaultProfile</span></span>
<span data-ttu-id="aa48e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa48e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa48e-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa48e-113">-Description</span></span>
<span data-ttu-id="aa48e-114">Descrizione dei criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="aa48e-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="aa48e-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="aa48e-115">-EnvironmentName</span></span>
<span data-ttu-id="aa48e-116">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="aa48e-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="aa48e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa48e-117">-Name</span></span>
<span data-ttu-id="aa48e-118">Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="aa48e-118">Name of the access policy.</span></span>

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

### <span data-ttu-id="aa48e-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="aa48e-119">-PrincipalObjectId</span></span>
<span data-ttu-id="aa48e-120">ObjectId dell'entità in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="aa48e-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="aa48e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa48e-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa48e-122">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="aa48e-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="aa48e-123">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="aa48e-123">-Role</span></span>
<span data-ttu-id="aa48e-124">Elenco dei ruoli assegnati all'oggetto Principal nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="aa48e-124">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="aa48e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa48e-125">-SubscriptionId</span></span>
<span data-ttu-id="aa48e-126">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="aa48e-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="aa48e-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aa48e-127">-Confirm</span></span>
<span data-ttu-id="aa48e-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa48e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa48e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa48e-129">-WhatIf</span></span>
<span data-ttu-id="aa48e-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa48e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa48e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa48e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa48e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa48e-132">CommonParameters</span></span>
<span data-ttu-id="aa48e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa48e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa48e-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa48e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa48e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa48e-135">INPUTS</span></span>

## <span data-ttu-id="aa48e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa48e-136">OUTPUTS</span></span>

### <span data-ttu-id="aa48e-137">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="aa48e-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="aa48e-138">Note</span><span class="sxs-lookup"><span data-stu-id="aa48e-138">NOTES</span></span>

<span data-ttu-id="aa48e-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="aa48e-139">ALIASES</span></span>

## <span data-ttu-id="aa48e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa48e-140">RELATED LINKS</span></span>
