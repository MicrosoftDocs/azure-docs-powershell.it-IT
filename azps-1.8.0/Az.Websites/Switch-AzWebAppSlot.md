---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 8f180eccd92a912820f8d3306ef735c84c30d3a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676241"
---
# <span data-ttu-id="18bc3-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="18bc3-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="18bc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="18bc3-103">Scambiare due slot con un'app Web</span><span class="sxs-lookup"><span data-stu-id="18bc3-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="18bc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18bc3-104">SYNTAX</span></span>

### <span data-ttu-id="18bc3-105">S1</span><span class="sxs-lookup"><span data-stu-id="18bc3-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18bc3-106">S2</span><span class="sxs-lookup"><span data-stu-id="18bc3-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18bc3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18bc3-107">DESCRIPTION</span></span>
<span data-ttu-id="18bc3-108">L' **opzione Switch-AzWebAppSlot** passa due slot associati a un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="18bc3-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="18bc3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18bc3-109">EXAMPLES</span></span>

### <span data-ttu-id="18bc3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="18bc3-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="18bc3-111">Questo comando commuta lo slot "sourceslot" con "destinationslot" per l'app Web ContosoWebApp associato al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="18bc3-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="18bc3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18bc3-112">PARAMETERS</span></span>

### <span data-ttu-id="18bc3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18bc3-113">-DefaultProfile</span></span>
<span data-ttu-id="18bc3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18bc3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18bc3-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="18bc3-115">-DestinationSlotName</span></span>
<span data-ttu-id="18bc3-116">Nome dello slot di destinazione</span><span class="sxs-lookup"><span data-stu-id="18bc3-116">Destination Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18bc3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="18bc3-117">-Name</span></span>
<span data-ttu-id="18bc3-118">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="18bc3-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bc3-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="18bc3-119">-PreserveVnet</span></span>
<span data-ttu-id="18bc3-120">Mantieni VNET booleano</span><span class="sxs-lookup"><span data-stu-id="18bc3-120">Preserve Vnet Boolean</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18bc3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18bc3-121">-ResourceGroupName</span></span>
<span data-ttu-id="18bc3-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="18bc3-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18bc3-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="18bc3-123">-SourceSlotName</span></span>
<span data-ttu-id="18bc3-124">Nome dello slot di origine</span><span class="sxs-lookup"><span data-stu-id="18bc3-124">Source Slot Name</span></span>

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

### <span data-ttu-id="18bc3-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="18bc3-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="18bc3-126">Scambiare con l'azione anteprima</span><span class="sxs-lookup"><span data-stu-id="18bc3-126">Swap With Preview Action</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.WebApps.Utilities.SwapWithPreviewAction]
Parameter Sets: (All)
Aliases:
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18bc3-127">-Web App</span><span class="sxs-lookup"><span data-stu-id="18bc3-127">-WebApp</span></span>
<span data-ttu-id="18bc3-128">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="18bc3-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18bc3-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18bc3-129">-Confirm</span></span>
<span data-ttu-id="18bc3-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18bc3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18bc3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18bc3-131">-WhatIf</span></span>
<span data-ttu-id="18bc3-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18bc3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18bc3-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18bc3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18bc3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18bc3-134">CommonParameters</span></span>
<span data-ttu-id="18bc3-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18bc3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18bc3-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18bc3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18bc3-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18bc3-137">INPUTS</span></span>

### <span data-ttu-id="18bc3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="18bc3-138">System.String</span></span>

### <span data-ttu-id="18bc3-139">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="18bc3-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="18bc3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18bc3-140">OUTPUTS</span></span>

### <span data-ttu-id="18bc3-141">System. void</span><span class="sxs-lookup"><span data-stu-id="18bc3-141">System.Void</span></span>

## <span data-ttu-id="18bc3-142">Note</span><span class="sxs-lookup"><span data-stu-id="18bc3-142">NOTES</span></span>

## <span data-ttu-id="18bc3-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18bc3-143">RELATED LINKS</span></span>
