---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 66c91c7a486638c01902f6091993143bb2e1a535
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192551"
---
# <span data-ttu-id="4161b-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="4161b-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="4161b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4161b-102">SYNOPSIS</span></span>
<span data-ttu-id="4161b-103">Configura un nuovo dispositivo Edge della casella dati</span><span class="sxs-lookup"><span data-stu-id="4161b-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="4161b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4161b-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4161b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4161b-105">DESCRIPTION</span></span>
<span data-ttu-id="4161b-106">Il cmdlet **New-AzDataBoxEdgeDevice** configura un nuovo dispositivo Edge della casella dati</span><span class="sxs-lookup"><span data-stu-id="4161b-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="4161b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4161b-107">EXAMPLES</span></span>

### <span data-ttu-id="4161b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4161b-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="4161b-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4161b-109">PARAMETERS</span></span>

### <span data-ttu-id="4161b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4161b-110">-AsJob</span></span>
<span data-ttu-id="4161b-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4161b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4161b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4161b-112">-DefaultProfile</span></span>
<span data-ttu-id="4161b-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4161b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4161b-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4161b-114">-Location</span></span>
<span data-ttu-id="4161b-115">Posizione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="4161b-115">Location of the device</span></span>

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

### <span data-ttu-id="4161b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4161b-116">-Name</span></span>
<span data-ttu-id="4161b-117">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="4161b-117">Resource Name</span></span>

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

### <span data-ttu-id="4161b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4161b-118">-ResourceGroupName</span></span>
<span data-ttu-id="4161b-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4161b-119">Resource Group Name</span></span>

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

### <span data-ttu-id="4161b-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="4161b-120">-Sku</span></span>
<span data-ttu-id="4161b-121">Le SKU disponibili sono Edge, gateway</span><span class="sxs-lookup"><span data-stu-id="4161b-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="4161b-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4161b-122">-Confirm</span></span>
<span data-ttu-id="4161b-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4161b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4161b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4161b-124">-WhatIf</span></span>
<span data-ttu-id="4161b-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4161b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4161b-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4161b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4161b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4161b-127">CommonParameters</span></span>
<span data-ttu-id="4161b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4161b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4161b-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4161b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4161b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4161b-130">INPUTS</span></span>

### <span data-ttu-id="4161b-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4161b-131">None</span></span>

## <span data-ttu-id="4161b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4161b-132">OUTPUTS</span></span>

### <span data-ttu-id="4161b-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="4161b-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="4161b-134">Note</span><span class="sxs-lookup"><span data-stu-id="4161b-134">NOTES</span></span>

## <span data-ttu-id="4161b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4161b-135">RELATED LINKS</span></span>
