---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: d808f7287a8ae3c03d86867f409d28820325e858
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677834"
---
# <span data-ttu-id="89b28-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="89b28-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="89b28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89b28-102">SYNOPSIS</span></span>
<span data-ttu-id="89b28-103">Interrompe la raccolta di registri IIS da computer.</span><span class="sxs-lookup"><span data-stu-id="89b28-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="89b28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89b28-104">SYNTAX</span></span>

### <span data-ttu-id="89b28-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="89b28-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89b28-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="89b28-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89b28-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89b28-107">DESCRIPTION</span></span>
<span data-ttu-id="89b28-108">Il cmdlet **Disable-AzOperationalInsightsIISLogCollection** interrompe la raccolta di registri Internet Information Services (IIS) da computer connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="89b28-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="89b28-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89b28-109">EXAMPLES</span></span>

## <span data-ttu-id="89b28-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89b28-110">PARAMETERS</span></span>

### <span data-ttu-id="89b28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b28-111">-DefaultProfile</span></span>
<span data-ttu-id="89b28-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="89b28-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89b28-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89b28-113">-ResourceGroupName</span></span>
<span data-ttu-id="89b28-114">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="89b28-114">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b28-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="89b28-115">-Workspace</span></span>
<span data-ttu-id="89b28-116">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89b28-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89b28-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="89b28-117">-WorkspaceName</span></span>
<span data-ttu-id="89b28-118">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89b28-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89b28-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="89b28-119">-Confirm</span></span>
<span data-ttu-id="89b28-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89b28-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b28-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89b28-121">-WhatIf</span></span>
<span data-ttu-id="89b28-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89b28-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89b28-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89b28-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89b28-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b28-124">CommonParameters</span></span>
<span data-ttu-id="89b28-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89b28-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b28-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89b28-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b28-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89b28-127">INPUTS</span></span>

### <span data-ttu-id="89b28-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="89b28-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="89b28-129">System. String</span><span class="sxs-lookup"><span data-stu-id="89b28-129">System.String</span></span>

## <span data-ttu-id="89b28-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89b28-130">OUTPUTS</span></span>

### <span data-ttu-id="89b28-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="89b28-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="89b28-132">Note</span><span class="sxs-lookup"><span data-stu-id="89b28-132">NOTES</span></span>
* <span data-ttu-id="89b28-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="89b28-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="89b28-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89b28-134">RELATED LINKS</span></span>

[<span data-ttu-id="89b28-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="89b28-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)


