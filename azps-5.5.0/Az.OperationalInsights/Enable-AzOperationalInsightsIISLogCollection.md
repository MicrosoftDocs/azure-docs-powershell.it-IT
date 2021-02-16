---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: f48007be3e1209cff65e46c669bce46298182247
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186774"
---
# <span data-ttu-id="5f37d-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="5f37d-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="5f37d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f37d-102">SYNOPSIS</span></span>
<span data-ttu-id="5f37d-103">Avvia la raccolta di log IIS dai computer di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5f37d-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="5f37d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f37d-104">SYNTAX</span></span>

### <span data-ttu-id="5f37d-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5f37d-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f37d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5f37d-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f37d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5f37d-107">DESCRIPTION</span></span>
<span data-ttu-id="5f37d-108">Il cmdlet **Enable-AzOperationalInsightsIISLogCollection** avvia la raccolta di log di Internet Information Services (IIS) dai computer connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5f37d-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="5f37d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f37d-109">EXAMPLES</span></span>

## <span data-ttu-id="5f37d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f37d-110">PARAMETERS</span></span>

### <span data-ttu-id="5f37d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f37d-111">-DefaultProfile</span></span>
<span data-ttu-id="5f37d-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5f37d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f37d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f37d-113">-ResourceGroupName</span></span>
<span data-ttu-id="5f37d-114">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="5f37d-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="5f37d-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="5f37d-115">-Workspace</span></span>
<span data-ttu-id="5f37d-116">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f37d-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5f37d-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5f37d-117">-WorkspaceName</span></span>
<span data-ttu-id="5f37d-118">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f37d-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5f37d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f37d-119">-Confirm</span></span>
<span data-ttu-id="5f37d-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f37d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f37d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f37d-121">-WhatIf</span></span>
<span data-ttu-id="5f37d-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f37d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f37d-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f37d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f37d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f37d-124">CommonParameters</span></span>
<span data-ttu-id="5f37d-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f37d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f37d-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f37d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f37d-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="5f37d-127">INPUTS</span></span>

### <span data-ttu-id="5f37d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5f37d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="5f37d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5f37d-129">System.String</span></span>

## <span data-ttu-id="5f37d-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f37d-130">OUTPUTS</span></span>

### <span data-ttu-id="5f37d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5f37d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5f37d-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="5f37d-132">NOTES</span></span>

## <span data-ttu-id="5f37d-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f37d-133">RELATED LINKS</span></span>

[<span data-ttu-id="5f37d-134">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="5f37d-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)


