---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: b9ab24915af941cec866fb78003d2b0e9c11267c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520014"
---
# <span data-ttu-id="84ad7-101">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="84ad7-101">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="84ad7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="84ad7-103">Avvia la raccolta di registri IIS da computer in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="84ad7-103">Starts collection of IIS logs from computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84ad7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84ad7-104">SYNTAX</span></span>

### <span data-ttu-id="84ad7-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84ad7-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84ad7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="84ad7-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84ad7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84ad7-107">DESCRIPTION</span></span>
<span data-ttu-id="84ad7-108">Il cmdlet **Enable-AzureRmOperationalInsightsIISLogCollection** avvia la raccolta di registri Internet Information Services (IIS) da computer connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="84ad7-108">The **Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="84ad7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84ad7-109">EXAMPLES</span></span>

## <span data-ttu-id="84ad7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84ad7-110">PARAMETERS</span></span>

### <span data-ttu-id="84ad7-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84ad7-111">-ResourceGroupName</span></span>
<span data-ttu-id="84ad7-112">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="84ad7-112">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="84ad7-113">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="84ad7-113">-Workspace</span></span>
<span data-ttu-id="84ad7-114">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84ad7-114">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="84ad7-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="84ad7-115">-WorkspaceName</span></span>
<span data-ttu-id="84ad7-116">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84ad7-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="84ad7-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="84ad7-117">-Confirm</span></span>
<span data-ttu-id="84ad7-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84ad7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84ad7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84ad7-119">-WhatIf</span></span>
<span data-ttu-id="84ad7-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84ad7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84ad7-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84ad7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84ad7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84ad7-122">-DefaultProfile</span></span>
<span data-ttu-id="84ad7-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84ad7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84ad7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84ad7-124">CommonParameters</span></span>
<span data-ttu-id="84ad7-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84ad7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84ad7-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84ad7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84ad7-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84ad7-127">INPUTS</span></span>

### <span data-ttu-id="84ad7-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="84ad7-128">PSWorkspace</span></span>
<span data-ttu-id="84ad7-129">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="84ad7-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="84ad7-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84ad7-130">OUTPUTS</span></span>

### <span data-ttu-id="84ad7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="84ad7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="84ad7-132">Note</span><span class="sxs-lookup"><span data-stu-id="84ad7-132">NOTES</span></span>

## <span data-ttu-id="84ad7-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84ad7-133">RELATED LINKS</span></span>

[<span data-ttu-id="84ad7-134">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="84ad7-134">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Disable-AzureRmOperationalInsightsIISLogCollection.md)


