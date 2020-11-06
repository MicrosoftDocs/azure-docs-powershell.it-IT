---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/switch-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
ms.openlocfilehash: ada4e30b69d4dcb6193db94e3f770966c15c5f70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514719"
---
# <span data-ttu-id="f47b2-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f47b2-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="f47b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f47b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f47b2-103">Scambiare due slot con un'app Web</span><span class="sxs-lookup"><span data-stu-id="f47b2-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f47b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f47b2-104">SYNTAX</span></span>

### <span data-ttu-id="f47b2-105">S1</span><span class="sxs-lookup"><span data-stu-id="f47b2-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f47b2-106">S2</span><span class="sxs-lookup"><span data-stu-id="f47b2-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f47b2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f47b2-107">DESCRIPTION</span></span>
<span data-ttu-id="f47b2-108">L' **opzione Switch-AzureRmWebAppSlot** passa due slot associati a un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="f47b2-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="f47b2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f47b2-109">EXAMPLES</span></span>

### <span data-ttu-id="f47b2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f47b2-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="f47b2-111">Questo comando commuta lo slot "sourceslot" con "destinationslot" per l'app Web ContosoWebApp associato al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="f47b2-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="f47b2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f47b2-112">PARAMETERS</span></span>

### <span data-ttu-id="f47b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f47b2-113">-DefaultProfile</span></span>
<span data-ttu-id="f47b2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f47b2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f47b2-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="f47b2-115">-DestinationSlotName</span></span>
<span data-ttu-id="f47b2-116">Nome dello slot di destinazione</span><span class="sxs-lookup"><span data-stu-id="f47b2-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="f47b2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f47b2-117">-Name</span></span>
<span data-ttu-id="f47b2-118">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="f47b2-118">WebApp Name</span></span>

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

### <span data-ttu-id="f47b2-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="f47b2-119">-PreserveVnet</span></span>
<span data-ttu-id="f47b2-120">Mantieni VNET booleano</span><span class="sxs-lookup"><span data-stu-id="f47b2-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="f47b2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f47b2-121">-ResourceGroupName</span></span>
<span data-ttu-id="f47b2-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f47b2-122">Resource Group Name</span></span>

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

### <span data-ttu-id="f47b2-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="f47b2-123">-SourceSlotName</span></span>
<span data-ttu-id="f47b2-124">Nome dello slot di origine</span><span class="sxs-lookup"><span data-stu-id="f47b2-124">Source Slot Name</span></span>

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

### <span data-ttu-id="f47b2-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="f47b2-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="f47b2-126">Scambiare con l'azione anteprima</span><span class="sxs-lookup"><span data-stu-id="f47b2-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="f47b2-127">-Web App</span><span class="sxs-lookup"><span data-stu-id="f47b2-127">-WebApp</span></span>
<span data-ttu-id="f47b2-128">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="f47b2-128">WebApp Object</span></span>

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

### <span data-ttu-id="f47b2-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f47b2-129">-Confirm</span></span>
<span data-ttu-id="f47b2-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f47b2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f47b2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f47b2-131">-WhatIf</span></span>
<span data-ttu-id="f47b2-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f47b2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f47b2-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f47b2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f47b2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f47b2-134">CommonParameters</span></span>
<span data-ttu-id="f47b2-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f47b2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f47b2-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f47b2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f47b2-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f47b2-137">INPUTS</span></span>

### <span data-ttu-id="f47b2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f47b2-138">System.String</span></span>

### <span data-ttu-id="f47b2-139">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="f47b2-139">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="f47b2-140">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f47b2-140">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="f47b2-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f47b2-141">OUTPUTS</span></span>

### <span data-ttu-id="f47b2-142">System. void</span><span class="sxs-lookup"><span data-stu-id="f47b2-142">System.Void</span></span>

## <span data-ttu-id="f47b2-143">Note</span><span class="sxs-lookup"><span data-stu-id="f47b2-143">NOTES</span></span>

## <span data-ttu-id="f47b2-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f47b2-144">RELATED LINKS</span></span>
