---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 085aa91321f9e263e4fa5620f982beb01eab2b16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685702"
---
# <span data-ttu-id="ab194-101">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="ab194-101">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="ab194-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab194-102">SYNOPSIS</span></span>
<span data-ttu-id="ab194-103">Interrompe la raccolta di registri IIS da computer.</span><span class="sxs-lookup"><span data-stu-id="ab194-103">Stops collection of IIS logs from computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab194-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab194-104">SYNTAX</span></span>

### <span data-ttu-id="ab194-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab194-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab194-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ab194-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab194-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab194-107">DESCRIPTION</span></span>
<span data-ttu-id="ab194-108">Il cmdlet **Disable-AzureRmOperationalInsightsIISLogCollection** interrompe la raccolta di registri Internet Information Services (IIS) da computer connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ab194-108">The **Disable-AzureRmOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="ab194-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab194-109">EXAMPLES</span></span>

## <span data-ttu-id="ab194-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab194-110">PARAMETERS</span></span>

### <span data-ttu-id="ab194-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab194-111">-DefaultProfile</span></span>
<span data-ttu-id="ab194-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ab194-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab194-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab194-113">-ResourceGroupName</span></span>
<span data-ttu-id="ab194-114">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="ab194-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="ab194-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ab194-115">-Workspace</span></span>
<span data-ttu-id="ab194-116">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab194-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ab194-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ab194-117">-WorkspaceName</span></span>
<span data-ttu-id="ab194-118">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab194-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ab194-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab194-119">-Confirm</span></span>
<span data-ttu-id="ab194-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab194-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab194-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab194-121">-WhatIf</span></span>
<span data-ttu-id="ab194-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab194-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab194-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab194-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab194-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab194-124">CommonParameters</span></span>
<span data-ttu-id="ab194-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab194-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab194-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab194-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab194-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab194-127">INPUTS</span></span>

### <span data-ttu-id="ab194-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ab194-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="ab194-129">Parametri: area di lavoro (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab194-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="ab194-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ab194-130">System.String</span></span>

## <span data-ttu-id="ab194-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab194-131">OUTPUTS</span></span>

### <span data-ttu-id="ab194-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ab194-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ab194-133">Note</span><span class="sxs-lookup"><span data-stu-id="ab194-133">NOTES</span></span>
* <span data-ttu-id="ab194-134">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="ab194-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="ab194-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab194-135">RELATED LINKS</span></span>

[<span data-ttu-id="ab194-136">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="ab194-136">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Enable-AzureRmOperationalInsightsIISLogCollection.md)


