---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 652a5668bd641ae1b68093f431e0aa0963aca50b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201607"
---
# <span data-ttu-id="9bf0d-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9bf0d-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="9bf0d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9bf0d-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf0d-103">Creare un account di archiviazione collegato dell'applicazione Insights</span><span class="sxs-lookup"><span data-stu-id="9bf0d-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="9bf0d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bf0d-104">SYNTAX</span></span>

### <span data-ttu-id="9bf0d-105">ByResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9bf0d-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bf0d-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bf0d-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bf0d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bf0d-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bf0d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bf0d-108">DESCRIPTION</span></span>
<span data-ttu-id="9bf0d-109">Creare un account di archiviazione collegato dell'applicazione Insights</span><span class="sxs-lookup"><span data-stu-id="9bf0d-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="9bf0d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bf0d-110">EXAMPLES</span></span>

### <span data-ttu-id="9bf0d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9bf0d-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="9bf0d-112">Creare un account di archiviazione collegato $account in componente "ComponentName"</span><span class="sxs-lookup"><span data-stu-id="9bf0d-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="9bf0d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9bf0d-113">PARAMETERS</span></span>

### <span data-ttu-id="9bf0d-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="9bf0d-114">-ComponentName</span></span>
<span data-ttu-id="9bf0d-115">Nome componente</span><span class="sxs-lookup"><span data-stu-id="9bf0d-115">Component Name</span></span>

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

### <span data-ttu-id="9bf0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf0d-116">-DefaultProfile</span></span>
<span data-ttu-id="9bf0d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bf0d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bf0d-118">-InputObject</span></span>
<span data-ttu-id="9bf0d-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9bf0d-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="9bf0d-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="9bf0d-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="9bf0d-121">ResourceId account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9bf0d-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="9bf0d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf0d-122">-ResourceGroupName</span></span>
<span data-ttu-id="9bf0d-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9bf0d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="9bf0d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bf0d-124">-ResourceId</span></span>
<span data-ttu-id="9bf0d-125">Componente ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bf0d-125">Component ResourceId</span></span>

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

### <span data-ttu-id="9bf0d-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9bf0d-126">-Confirm</span></span>
<span data-ttu-id="9bf0d-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bf0d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bf0d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bf0d-128">-WhatIf</span></span>
<span data-ttu-id="9bf0d-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bf0d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bf0d-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bf0d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bf0d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf0d-131">CommonParameters</span></span>
<span data-ttu-id="9bf0d-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf0d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf0d-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bf0d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf0d-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9bf0d-134">INPUTS</span></span>

### <span data-ttu-id="9bf0d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9bf0d-135">System.String</span></span>

### <span data-ttu-id="9bf0d-136">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9bf0d-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="9bf0d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bf0d-137">OUTPUTS</span></span>

### <span data-ttu-id="9bf0d-138">Microsoft. Azure. Commands. ApplicationInsights. Models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="9bf0d-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="9bf0d-139">Note</span><span class="sxs-lookup"><span data-stu-id="9bf0d-139">NOTES</span></span>

## <span data-ttu-id="9bf0d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bf0d-140">RELATED LINKS</span></span>
