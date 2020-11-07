---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/switch-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 9671c2041f767df5066353988eb633318289de47
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865982"
---
# <span data-ttu-id="0f0fa-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0f0fa-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="0f0fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f0fa-102">SYNOPSIS</span></span>
<span data-ttu-id="0f0fa-103">Scambiare due slot con un'app Web</span><span class="sxs-lookup"><span data-stu-id="0f0fa-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f0fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f0fa-104">SYNTAX</span></span>

### <span data-ttu-id="0f0fa-105">S1</span><span class="sxs-lookup"><span data-stu-id="0f0fa-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f0fa-106">S2</span><span class="sxs-lookup"><span data-stu-id="0f0fa-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f0fa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f0fa-107">DESCRIPTION</span></span>
<span data-ttu-id="0f0fa-108">L' **opzione Switch-AzureRmWebAppSlot** passa due slot associati a un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="0f0fa-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="0f0fa-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f0fa-109">EXAMPLES</span></span>

### <span data-ttu-id="0f0fa-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f0fa-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="0f0fa-111">Questo comando commuta lo slot "sourceslot" con "destinationslot" per l'app Web ContosoWebApp associato al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="0f0fa-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="0f0fa-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f0fa-112">PARAMETERS</span></span>

### <span data-ttu-id="0f0fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f0fa-113">-DefaultProfile</span></span>
<span data-ttu-id="0f0fa-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f0fa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f0fa-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="0f0fa-115">-DestinationSlotName</span></span>
<span data-ttu-id="0f0fa-116">Nome dello slot di destinazione</span><span class="sxs-lookup"><span data-stu-id="0f0fa-116">Destination Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0fa-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f0fa-117">-Name</span></span>
<span data-ttu-id="0f0fa-118">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="0f0fa-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0fa-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="0f0fa-119">-PreserveVnet</span></span>
<span data-ttu-id="0f0fa-120">Mantieni VNET booleano</span><span class="sxs-lookup"><span data-stu-id="0f0fa-120">Preserve Vnet Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0fa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f0fa-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f0fa-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="0f0fa-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0fa-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="0f0fa-123">-SourceSlotName</span></span>
<span data-ttu-id="0f0fa-124">Nome dello slot di origine</span><span class="sxs-lookup"><span data-stu-id="0f0fa-124">Source Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0fa-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="0f0fa-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="0f0fa-126">Scambiare con l'azione anteprima</span><span class="sxs-lookup"><span data-stu-id="0f0fa-126">Swap With Preview Action</span></span>

```yaml
Type: SwapWithPreviewAction
Parameter Sets: (All)
Aliases: 
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0fa-127">-Web App</span><span class="sxs-lookup"><span data-stu-id="0f0fa-127">-WebApp</span></span>
<span data-ttu-id="0f0fa-128">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="0f0fa-128">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0fa-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0f0fa-129">-Confirm</span></span>
<span data-ttu-id="0f0fa-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f0fa-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0fa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f0fa-131">-WhatIf</span></span>
<span data-ttu-id="0f0fa-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f0fa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f0fa-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f0fa-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0fa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f0fa-134">CommonParameters</span></span>
<span data-ttu-id="0f0fa-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f0fa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f0fa-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f0fa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f0fa-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f0fa-137">INPUTS</span></span>

### <span data-ttu-id="0f0fa-138">Sito</span><span class="sxs-lookup"><span data-stu-id="0f0fa-138">Site</span></span>
<span data-ttu-id="0f0fa-139">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0f0fa-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0f0fa-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f0fa-140">OUTPUTS</span></span>

## <span data-ttu-id="0f0fa-141">Note</span><span class="sxs-lookup"><span data-stu-id="0f0fa-141">NOTES</span></span>

## <span data-ttu-id="0f0fa-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f0fa-142">RELATED LINKS</span></span>

