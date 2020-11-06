---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 2b6bc41feb283e4a9f4be18f65c9a5be127598e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511640"
---
# <span data-ttu-id="ff54a-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="ff54a-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="ff54a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff54a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff54a-103">Avvia la raccolta di registri personalizzati da computer Linux.</span><span class="sxs-lookup"><span data-stu-id="ff54a-103">Starts collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff54a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff54a-104">SYNTAX</span></span>

### <span data-ttu-id="ff54a-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff54a-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff54a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ff54a-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff54a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff54a-107">DESCRIPTION</span></span>
<span data-ttu-id="ff54a-108">Il cmdlet **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** avvia la raccolta di registri personalizzati da computer Linux connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ff54a-108">The **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="ff54a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff54a-109">EXAMPLES</span></span>

## <span data-ttu-id="ff54a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff54a-110">PARAMETERS</span></span>

### <span data-ttu-id="ff54a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff54a-111">-DefaultProfile</span></span>
<span data-ttu-id="ff54a-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ff54a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff54a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff54a-113">-ResourceGroupName</span></span>
<span data-ttu-id="ff54a-114">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="ff54a-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="ff54a-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ff54a-115">-Workspace</span></span>
<span data-ttu-id="ff54a-116">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff54a-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ff54a-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ff54a-117">-WorkspaceName</span></span>
<span data-ttu-id="ff54a-118">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff54a-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ff54a-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ff54a-119">-Confirm</span></span>
<span data-ttu-id="ff54a-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff54a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff54a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff54a-121">-WhatIf</span></span>
<span data-ttu-id="ff54a-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff54a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff54a-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff54a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff54a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff54a-124">CommonParameters</span></span>
<span data-ttu-id="ff54a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff54a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff54a-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff54a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff54a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff54a-127">INPUTS</span></span>

### <span data-ttu-id="ff54a-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ff54a-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="ff54a-129">Parametri: area di lavoro (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ff54a-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="ff54a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ff54a-130">System.String</span></span>

## <span data-ttu-id="ff54a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff54a-131">OUTPUTS</span></span>

### <span data-ttu-id="ff54a-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ff54a-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ff54a-133">Note</span><span class="sxs-lookup"><span data-stu-id="ff54a-133">NOTES</span></span>
* <span data-ttu-id="ff54a-134">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="ff54a-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="ff54a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff54a-135">RELATED LINKS</span></span>

[<span data-ttu-id="ff54a-136">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="ff54a-136">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


