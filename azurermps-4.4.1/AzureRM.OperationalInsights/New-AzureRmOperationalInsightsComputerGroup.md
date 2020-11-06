---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 8a54a735b41ef537a31f5e3e1ce2789d10e60af6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516151"
---
# <span data-ttu-id="d194f-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="d194f-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="d194f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d194f-102">SYNOPSIS</span></span>
<span data-ttu-id="d194f-103">Crea un gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="d194f-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d194f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d194f-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d194f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d194f-105">DESCRIPTION</span></span>
<span data-ttu-id="d194f-106">Il cmdlet **New-AzureRmOperationalInsightsComputerGroup** crea un gruppo di computer in un gruppo di risorse e una posizione.</span><span class="sxs-lookup"><span data-stu-id="d194f-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="d194f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d194f-107">EXAMPLES</span></span>

## <span data-ttu-id="d194f-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d194f-108">PARAMETERS</span></span>

### <span data-ttu-id="d194f-109">-Categoria</span><span class="sxs-lookup"><span data-stu-id="d194f-109">-Category</span></span>
<span data-ttu-id="d194f-110">Specifica la categoria del gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="d194f-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="d194f-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d194f-111">-DisplayName</span></span>
<span data-ttu-id="d194f-112">Specifica il nome visualizzato del gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="d194f-112">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="d194f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d194f-113">-Force</span></span>
<span data-ttu-id="d194f-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d194f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d194f-115">-Query</span><span class="sxs-lookup"><span data-stu-id="d194f-115">-Query</span></span>
<span data-ttu-id="d194f-116">Specifica la query del gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="d194f-116">Specifies the query of the computer group.</span></span>

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

### <span data-ttu-id="d194f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d194f-117">-ResourceGroupName</span></span>
<span data-ttu-id="d194f-118">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="d194f-118">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d194f-119">Il cmdlet crea un gruppo di computer in questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d194f-119">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="d194f-120">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="d194f-120">-SavedSearchId</span></span>
<span data-ttu-id="d194f-121">Specifica l'ID del gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="d194f-121">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="d194f-122">-Versione</span><span class="sxs-lookup"><span data-stu-id="d194f-122">-Version</span></span>
<span data-ttu-id="d194f-123">Specifica la versione.</span><span class="sxs-lookup"><span data-stu-id="d194f-123">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d194f-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d194f-124">-WorkspaceName</span></span>
<span data-ttu-id="d194f-125">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d194f-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="d194f-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d194f-126">-Confirm</span></span>
<span data-ttu-id="d194f-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d194f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d194f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d194f-128">-WhatIf</span></span>
<span data-ttu-id="d194f-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d194f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d194f-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d194f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d194f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d194f-131">-DefaultProfile</span></span>
<span data-ttu-id="d194f-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d194f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d194f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d194f-133">CommonParameters</span></span>
<span data-ttu-id="d194f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d194f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d194f-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d194f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d194f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d194f-136">INPUTS</span></span>

## <span data-ttu-id="d194f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d194f-137">OUTPUTS</span></span>

## <span data-ttu-id="d194f-138">Note</span><span class="sxs-lookup"><span data-stu-id="d194f-138">NOTES</span></span>

## <span data-ttu-id="d194f-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d194f-139">RELATED LINKS</span></span>

