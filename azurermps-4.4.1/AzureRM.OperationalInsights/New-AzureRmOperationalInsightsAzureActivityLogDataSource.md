---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 15138ee817cddb992f5b6bbe0beccee10620ffdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516155"
---
# <span data-ttu-id="7709c-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="7709c-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="7709c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7709c-102">SYNOPSIS</span></span>
<span data-ttu-id="7709c-103">Raccogliere il log delle attività di Azure da un abbonamento specifico.</span><span class="sxs-lookup"><span data-stu-id="7709c-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7709c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7709c-104">SYNTAX</span></span>

### <span data-ttu-id="7709c-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7709c-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7709c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7709c-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7709c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7709c-107">DESCRIPTION</span></span>
<span data-ttu-id="7709c-108">L'New-AzureRmOperationalInsightsAzureActivityLogDataSource Abilita analisi log per raccogliere il log delle attività di Azure da un abbonamento specifico.</span><span class="sxs-lookup"><span data-stu-id="7709c-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="7709c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7709c-109">EXAMPLES</span></span>

### <span data-ttu-id="7709c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7709c-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7709c-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="7709c-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="7709c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7709c-112">PARAMETERS</span></span>

### <span data-ttu-id="7709c-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="7709c-113">-BackfillStartTime</span></span>
<span data-ttu-id="7709c-114">È possibile scegliere di riempire i log di una settimana fa.</span><span class="sxs-lookup"><span data-stu-id="7709c-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7709c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7709c-115">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7709c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7709c-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7709c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7709c-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="7709c-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7709c-118">-SubscriptionId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7709c-119">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="7709c-119">-Workspace</span></span>
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

### <span data-ttu-id="7709c-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7709c-120">-WorkspaceName</span></span>
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

### <span data-ttu-id="7709c-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7709c-121">-Confirm</span></span>
<span data-ttu-id="7709c-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7709c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7709c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7709c-123">-WhatIf</span></span>
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

### <span data-ttu-id="7709c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7709c-124">-DefaultProfile</span></span>
<span data-ttu-id="7709c-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7709c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7709c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7709c-126">CommonParameters</span></span>
<span data-ttu-id="7709c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7709c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7709c-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7709c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7709c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7709c-129">INPUTS</span></span>

### <span data-ttu-id="7709c-130">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7709c-130">PSWorkspace</span></span>
<span data-ttu-id="7709c-131">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7709c-131">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="7709c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7709c-132">OUTPUTS</span></span>

### <span data-ttu-id="7709c-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7709c-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7709c-134">Note</span><span class="sxs-lookup"><span data-stu-id="7709c-134">NOTES</span></span>

## <span data-ttu-id="7709c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7709c-135">RELATED LINKS</span></span>

