---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191685"
---
# <span data-ttu-id="1dc3c-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1dc3c-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="1dc3c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1dc3c-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc3c-103">Eliminare l'account di archiviazione collegato agli Insight dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="1dc3c-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="1dc3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dc3c-104">SYNTAX</span></span>

### <span data-ttu-id="1dc3c-105">ByResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1dc3c-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc3c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc3c-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc3c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc3c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dc3c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dc3c-108">DESCRIPTION</span></span>
<span data-ttu-id="1dc3c-109">Eliminare l'account di archiviazione collegato agli Insight dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="1dc3c-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="1dc3c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dc3c-110">EXAMPLES</span></span>

### <span data-ttu-id="1dc3c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1dc3c-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="1dc3c-112">Eliminare l'account di archiviazione collegata associato al componente Insights applicazione "ComponentName"</span><span class="sxs-lookup"><span data-stu-id="1dc3c-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="1dc3c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1dc3c-113">PARAMETERS</span></span>

### <span data-ttu-id="1dc3c-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="1dc3c-114">-ComponentName</span></span>
<span data-ttu-id="1dc3c-115">Nome componente</span><span class="sxs-lookup"><span data-stu-id="1dc3c-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc3c-116">-DefaultProfile</span></span>
<span data-ttu-id="1dc3c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc3c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dc3c-118">-InputObject</span></span>
<span data-ttu-id="1dc3c-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1dc3c-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc3c-120">-ResourceGroupName</span></span>
<span data-ttu-id="1dc3c-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1dc3c-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dc3c-122">-ResourceId</span></span>
<span data-ttu-id="1dc3c-123">Componente ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dc3c-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3c-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1dc3c-124">-Confirm</span></span>
<span data-ttu-id="1dc3c-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dc3c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc3c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc3c-126">-WhatIf</span></span>
<span data-ttu-id="1dc3c-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dc3c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc3c-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dc3c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc3c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc3c-129">CommonParameters</span></span>
<span data-ttu-id="1dc3c-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc3c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc3c-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dc3c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc3c-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1dc3c-132">INPUTS</span></span>

### <span data-ttu-id="1dc3c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1dc3c-133">System.String</span></span>

### <span data-ttu-id="1dc3c-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1dc3c-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="1dc3c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dc3c-135">OUTPUTS</span></span>

### <span data-ttu-id="1dc3c-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1dc3c-136">System.Boolean</span></span>

## <span data-ttu-id="1dc3c-137">Note</span><span class="sxs-lookup"><span data-stu-id="1dc3c-137">NOTES</span></span>

## <span data-ttu-id="1dc3c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dc3c-138">RELATED LINKS</span></span>
