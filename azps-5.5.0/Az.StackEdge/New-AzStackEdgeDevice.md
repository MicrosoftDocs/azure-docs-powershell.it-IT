---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178279"
---
# <span data-ttu-id="67d6a-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="67d6a-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="67d6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="67d6a-103">Configura un nuovo dispositivo Stack Edge</span><span class="sxs-lookup"><span data-stu-id="67d6a-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="67d6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67d6a-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67d6a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67d6a-105">DESCRIPTION</span></span>
<span data-ttu-id="67d6a-106">Il cmdlet **New-AzStackEdgeDevice** configura un nuovo dispositivo Stack Edge</span><span class="sxs-lookup"><span data-stu-id="67d6a-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="67d6a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67d6a-107">EXAMPLES</span></span>

### <span data-ttu-id="67d6a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="67d6a-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="67d6a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67d6a-109">PARAMETERS</span></span>

### <span data-ttu-id="67d6a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67d6a-110">-AsJob</span></span>
<span data-ttu-id="67d6a-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="67d6a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67d6a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d6a-112">-DefaultProfile</span></span>
<span data-ttu-id="67d6a-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67d6a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67d6a-114">-Location</span><span class="sxs-lookup"><span data-stu-id="67d6a-114">-Location</span></span>
<span data-ttu-id="67d6a-115">Posizione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="67d6a-115">Location of the device</span></span>

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

### <span data-ttu-id="67d6a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="67d6a-116">-Name</span></span>
<span data-ttu-id="67d6a-117">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="67d6a-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d6a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d6a-118">-ResourceGroupName</span></span>
<span data-ttu-id="67d6a-119">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="67d6a-119">Resource Group Name</span></span>

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

### <span data-ttu-id="67d6a-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="67d6a-120">-Sku</span></span>
<span data-ttu-id="67d6a-121">Le SKU disponibili sono Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="67d6a-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="67d6a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67d6a-122">-Confirm</span></span>
<span data-ttu-id="67d6a-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d6a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67d6a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67d6a-124">-WhatIf</span></span>
<span data-ttu-id="67d6a-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67d6a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67d6a-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67d6a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67d6a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d6a-127">CommonParameters</span></span>
<span data-ttu-id="67d6a-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d6a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d6a-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="67d6a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d6a-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="67d6a-130">INPUTS</span></span>

### <span data-ttu-id="67d6a-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="67d6a-131">None</span></span>

## <span data-ttu-id="67d6a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67d6a-132">OUTPUTS</span></span>

### <span data-ttu-id="67d6a-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="67d6a-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="67d6a-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="67d6a-134">NOTES</span></span>

## <span data-ttu-id="67d6a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67d6a-135">RELATED LINKS</span></span>
