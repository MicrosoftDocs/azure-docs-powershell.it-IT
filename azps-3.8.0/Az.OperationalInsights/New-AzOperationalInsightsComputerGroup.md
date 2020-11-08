---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
ms.openlocfilehash: 299c91e1db10aaabda7c7dfadf856b445d1b2993
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018597"
---
# <span data-ttu-id="1f00a-101">New-AzOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="1f00a-101">New-AzOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="1f00a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f00a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f00a-103">Crea un gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="1f00a-103">Creates a computer group.</span></span>

## <span data-ttu-id="1f00a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f00a-104">SYNTAX</span></span>

```
New-AzOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f00a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f00a-105">DESCRIPTION</span></span>
<span data-ttu-id="1f00a-106">Il cmdlet **New-AzOperationalInsightsComputerGroup** crea un gruppo di computer in un gruppo di risorse e una posizione.</span><span class="sxs-lookup"><span data-stu-id="1f00a-106">The **New-AzOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="1f00a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f00a-107">EXAMPLES</span></span>

## <span data-ttu-id="1f00a-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f00a-108">PARAMETERS</span></span>

### <span data-ttu-id="1f00a-109">-Categoria</span><span class="sxs-lookup"><span data-stu-id="1f00a-109">-Category</span></span>
<span data-ttu-id="1f00a-110">Specifica la categoria del gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="1f00a-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="1f00a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f00a-111">-DefaultProfile</span></span>
<span data-ttu-id="1f00a-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1f00a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f00a-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f00a-113">-DisplayName</span></span>
<span data-ttu-id="1f00a-114">Specifica il nome visualizzato del gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="1f00a-114">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="1f00a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1f00a-115">-Force</span></span>
<span data-ttu-id="1f00a-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1f00a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f00a-117">-Query</span><span class="sxs-lookup"><span data-stu-id="1f00a-117">-Query</span></span>
<span data-ttu-id="1f00a-118">Specifica la query del gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="1f00a-118">Specifies the query of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f00a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f00a-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f00a-120">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="1f00a-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1f00a-121">Il cmdlet crea un gruppo di computer in questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f00a-121">The cmdlet creates computer group in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f00a-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="1f00a-122">-SavedSearchId</span></span>
<span data-ttu-id="1f00a-123">Specifica l'ID del gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="1f00a-123">Specifies the ID of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f00a-124">-Versione</span><span class="sxs-lookup"><span data-stu-id="1f00a-124">-Version</span></span>
<span data-ttu-id="1f00a-125">Specifica la versione.</span><span class="sxs-lookup"><span data-stu-id="1f00a-125">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f00a-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1f00a-126">-WorkspaceName</span></span>
<span data-ttu-id="1f00a-127">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1f00a-127">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f00a-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f00a-128">-Confirm</span></span>
<span data-ttu-id="1f00a-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f00a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f00a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f00a-130">-WhatIf</span></span>
<span data-ttu-id="1f00a-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f00a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f00a-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f00a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f00a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f00a-133">CommonParameters</span></span>
<span data-ttu-id="1f00a-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f00a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f00a-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f00a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f00a-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f00a-136">INPUTS</span></span>

### <span data-ttu-id="1f00a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1f00a-137">System.String</span></span>

### <span data-ttu-id="1f00a-138">System. Int64</span><span class="sxs-lookup"><span data-stu-id="1f00a-138">System.Int64</span></span>

## <span data-ttu-id="1f00a-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f00a-139">OUTPUTS</span></span>

### <span data-ttu-id="1f00a-140">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="1f00a-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="1f00a-141">Note</span><span class="sxs-lookup"><span data-stu-id="1f00a-141">NOTES</span></span>

## <span data-ttu-id="1f00a-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f00a-142">RELATED LINKS</span></span>
