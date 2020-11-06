---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: b76e17169bdea8e25c1b861cd7de802d877455f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511643"
---
# <span data-ttu-id="0f0db-101">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="0f0db-101">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="0f0db-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f0db-102">SYNOPSIS</span></span>
<span data-ttu-id="0f0db-103">Avvia la raccolta di registri IIS da computer in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0f0db-103">Starts collection of IIS logs from computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f0db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f0db-104">SYNTAX</span></span>

### <span data-ttu-id="0f0db-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f0db-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f0db-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0f0db-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f0db-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f0db-107">DESCRIPTION</span></span>
<span data-ttu-id="0f0db-108">Il cmdlet **Enable-AzureRmOperationalInsightsIISLogCollection** avvia la raccolta di registri Internet Information Services (IIS) da computer connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0f0db-108">The **Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="0f0db-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f0db-109">EXAMPLES</span></span>

## <span data-ttu-id="0f0db-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f0db-110">PARAMETERS</span></span>

### <span data-ttu-id="0f0db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f0db-111">-DefaultProfile</span></span>
<span data-ttu-id="0f0db-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0f0db-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0db-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f0db-113">-ResourceGroupName</span></span>
<span data-ttu-id="0f0db-114">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="0f0db-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="0f0db-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="0f0db-115">-Workspace</span></span>
<span data-ttu-id="0f0db-116">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f0db-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0f0db-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0f0db-117">-WorkspaceName</span></span>
<span data-ttu-id="0f0db-118">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f0db-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0f0db-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0f0db-119">-Confirm</span></span>
<span data-ttu-id="0f0db-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f0db-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f0db-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f0db-121">-WhatIf</span></span>
<span data-ttu-id="0f0db-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f0db-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f0db-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f0db-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f0db-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f0db-124">CommonParameters</span></span>
<span data-ttu-id="0f0db-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f0db-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f0db-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f0db-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f0db-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f0db-127">INPUTS</span></span>

### <span data-ttu-id="0f0db-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0f0db-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="0f0db-129">Parametri: area di lavoro (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f0db-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="0f0db-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0f0db-130">System.String</span></span>

## <span data-ttu-id="0f0db-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f0db-131">OUTPUTS</span></span>

### <span data-ttu-id="0f0db-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0f0db-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0f0db-133">Note</span><span class="sxs-lookup"><span data-stu-id="0f0db-133">NOTES</span></span>

## <span data-ttu-id="0f0db-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f0db-134">RELATED LINKS</span></span>

[<span data-ttu-id="0f0db-135">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="0f0db-135">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Disable-AzureRmOperationalInsightsIISLogCollection.md)


