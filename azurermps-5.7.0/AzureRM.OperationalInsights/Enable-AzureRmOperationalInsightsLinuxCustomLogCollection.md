---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 74178c9818cb5782c105e5566fd5e5dc44ef6526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521413"
---
# <span data-ttu-id="ddd4d-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="ddd4d-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="ddd4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddd4d-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd4d-103">Avvia la raccolta di registri personalizzati da computer Linux.</span><span class="sxs-lookup"><span data-stu-id="ddd4d-103">Starts collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddd4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddd4d-104">SYNTAX</span></span>

### <span data-ttu-id="ddd4d-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ddd4d-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd4d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ddd4d-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd4d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddd4d-107">DESCRIPTION</span></span>
<span data-ttu-id="ddd4d-108">Il cmdlet **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** avvia la raccolta di registri personalizzati da computer Linux connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ddd4d-108">The **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="ddd4d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddd4d-109">EXAMPLES</span></span>

## <span data-ttu-id="ddd4d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddd4d-110">PARAMETERS</span></span>

### <span data-ttu-id="ddd4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd4d-111">-DefaultProfile</span></span>
<span data-ttu-id="ddd4d-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ddd4d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd4d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd4d-113">-ResourceGroupName</span></span>
<span data-ttu-id="ddd4d-114">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="ddd4d-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd4d-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ddd4d-115">-Workspace</span></span>
<span data-ttu-id="ddd4d-116">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddd4d-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd4d-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ddd4d-117">-WorkspaceName</span></span>
<span data-ttu-id="ddd4d-118">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddd4d-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd4d-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ddd4d-119">-Confirm</span></span>
<span data-ttu-id="ddd4d-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddd4d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd4d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd4d-121">-WhatIf</span></span>
<span data-ttu-id="ddd4d-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddd4d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd4d-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddd4d-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd4d-124">CommonParameters</span></span>
<span data-ttu-id="ddd4d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd4d-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd4d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd4d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddd4d-127">INPUTS</span></span>

### <span data-ttu-id="ddd4d-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ddd4d-128">PSWorkspace</span></span>
<span data-ttu-id="ddd4d-129">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ddd4d-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="ddd4d-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddd4d-130">OUTPUTS</span></span>

### <span data-ttu-id="ddd4d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ddd4d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ddd4d-132">Note</span><span class="sxs-lookup"><span data-stu-id="ddd4d-132">NOTES</span></span>
* <span data-ttu-id="ddd4d-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="ddd4d-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="ddd4d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddd4d-134">RELATED LINKS</span></span>

[<span data-ttu-id="ddd4d-135">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="ddd4d-135">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

