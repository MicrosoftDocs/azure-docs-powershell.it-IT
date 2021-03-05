---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: b7deb19377d893d28d5b5924acf8c49daf706907
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978685"
---
# <span data-ttu-id="b1f32-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b1f32-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="b1f32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1f32-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f32-103">Configura un nuovo dispositivo Microsoft Data Box Edge</span><span class="sxs-lookup"><span data-stu-id="b1f32-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="b1f32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1f32-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1f32-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b1f32-105">DESCRIPTION</span></span>
<span data-ttu-id="b1f32-106">Il cmdlet **New-AzDataBoxEdgeDevice** configura un nuovo dispositivo Data Box Edge</span><span class="sxs-lookup"><span data-stu-id="b1f32-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="b1f32-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1f32-107">EXAMPLES</span></span>

### <span data-ttu-id="b1f32-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b1f32-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="b1f32-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1f32-109">PARAMETERS</span></span>

### <span data-ttu-id="b1f32-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1f32-110">-AsJob</span></span>
<span data-ttu-id="b1f32-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b1f32-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1f32-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f32-112">-DefaultProfile</span></span>
<span data-ttu-id="b1f32-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1f32-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1f32-114">-Location</span><span class="sxs-lookup"><span data-stu-id="b1f32-114">-Location</span></span>
<span data-ttu-id="b1f32-115">Posizione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b1f32-115">Location of the device</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f32-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b1f32-116">-Name</span></span>
<span data-ttu-id="b1f32-117">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="b1f32-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f32-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f32-118">-ResourceGroupName</span></span>
<span data-ttu-id="b1f32-119">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b1f32-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f32-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="b1f32-120">-Sku</span></span>
<span data-ttu-id="b1f32-121">Le SKU disponibili sono Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="b1f32-121">Available Skus are Edge, Gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f32-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1f32-122">-Confirm</span></span>
<span data-ttu-id="b1f32-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1f32-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1f32-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1f32-124">-WhatIf</span></span>
<span data-ttu-id="b1f32-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1f32-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1f32-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1f32-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1f32-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f32-127">CommonParameters</span></span>
<span data-ttu-id="b1f32-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f32-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f32-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1f32-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f32-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="b1f32-130">INPUTS</span></span>

### <span data-ttu-id="b1f32-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b1f32-131">None</span></span>

## <span data-ttu-id="b1f32-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1f32-132">OUTPUTS</span></span>

### <span data-ttu-id="b1f32-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b1f32-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="b1f32-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="b1f32-134">NOTES</span></span>

## <span data-ttu-id="b1f32-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1f32-135">RELATED LINKS</span></span>
