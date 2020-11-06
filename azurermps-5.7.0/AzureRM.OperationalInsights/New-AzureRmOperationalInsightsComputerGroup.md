---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 999e9e5fd9f0b93e71b222f228b1575e0492073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520678"
---
# <span data-ttu-id="ad80b-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="ad80b-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="ad80b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad80b-102">SYNOPSIS</span></span>
<span data-ttu-id="ad80b-103">Crea un gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="ad80b-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad80b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad80b-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad80b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad80b-105">DESCRIPTION</span></span>
<span data-ttu-id="ad80b-106">Il cmdlet **New-AzureRmOperationalInsightsComputerGroup** crea un gruppo di computer in un gruppo di risorse e una posizione.</span><span class="sxs-lookup"><span data-stu-id="ad80b-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="ad80b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad80b-107">EXAMPLES</span></span>

## <span data-ttu-id="ad80b-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad80b-108">PARAMETERS</span></span>

### <span data-ttu-id="ad80b-109">-Categoria</span><span class="sxs-lookup"><span data-stu-id="ad80b-109">-Category</span></span>
<span data-ttu-id="ad80b-110">Specifica la categoria del gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="ad80b-110">Specifies the category of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad80b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad80b-111">-DefaultProfile</span></span>
<span data-ttu-id="ad80b-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ad80b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad80b-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ad80b-113">-DisplayName</span></span>
<span data-ttu-id="ad80b-114">Specifica il nome visualizzato del gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="ad80b-114">Specifies the display name of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad80b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ad80b-115">-Force</span></span>
<span data-ttu-id="ad80b-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ad80b-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad80b-117">-Query</span><span class="sxs-lookup"><span data-stu-id="ad80b-117">-Query</span></span>
<span data-ttu-id="ad80b-118">Specifica la query del gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="ad80b-118">Specifies the query of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad80b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad80b-119">-ResourceGroupName</span></span>
<span data-ttu-id="ad80b-120">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="ad80b-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ad80b-121">Il cmdlet crea un gruppo di computer in questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad80b-121">The cmdlet creates computer group in this resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad80b-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="ad80b-122">-SavedSearchId</span></span>
<span data-ttu-id="ad80b-123">Specifica l'ID del gruppo di computer.</span><span class="sxs-lookup"><span data-stu-id="ad80b-123">Specifies the ID of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad80b-124">-Versione</span><span class="sxs-lookup"><span data-stu-id="ad80b-124">-Version</span></span>
<span data-ttu-id="ad80b-125">Specifica la versione.</span><span class="sxs-lookup"><span data-stu-id="ad80b-125">Specifies the version.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad80b-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ad80b-126">-WorkspaceName</span></span>
<span data-ttu-id="ad80b-127">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ad80b-127">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad80b-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ad80b-128">-Confirm</span></span>
<span data-ttu-id="ad80b-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad80b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad80b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad80b-130">-WhatIf</span></span>
<span data-ttu-id="ad80b-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad80b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad80b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad80b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad80b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad80b-133">CommonParameters</span></span>
<span data-ttu-id="ad80b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad80b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad80b-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad80b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad80b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad80b-136">INPUTS</span></span>

### <span data-ttu-id="ad80b-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ad80b-137">None</span></span>
<span data-ttu-id="ad80b-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ad80b-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad80b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad80b-139">OUTPUTS</span></span>

## <span data-ttu-id="ad80b-140">Note</span><span class="sxs-lookup"><span data-stu-id="ad80b-140">NOTES</span></span>

## <span data-ttu-id="ad80b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad80b-141">RELATED LINKS</span></span>

