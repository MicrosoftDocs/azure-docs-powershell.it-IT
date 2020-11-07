---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
ms.openlocfilehash: 9522fe6925ac266ff87f3ba6b3540980d91c160f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688597"
---
# <span data-ttu-id="85a00-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="85a00-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="85a00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85a00-102">SYNOPSIS</span></span>
<span data-ttu-id="85a00-103">Scambiare due slot con un'app Web</span><span class="sxs-lookup"><span data-stu-id="85a00-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85a00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85a00-104">SYNTAX</span></span>

### <span data-ttu-id="85a00-105">S1</span><span class="sxs-lookup"><span data-stu-id="85a00-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a00-106">S2</span><span class="sxs-lookup"><span data-stu-id="85a00-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85a00-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85a00-107">DESCRIPTION</span></span>
<span data-ttu-id="85a00-108">L' **opzione Switch-AzureRmWebAppSlot** passa due slot associati a un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="85a00-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="85a00-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85a00-109">EXAMPLES</span></span>

### <span data-ttu-id="85a00-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="85a00-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="85a00-111">Questo comando commuta lo slot "sourceslot" con "destinationslot" per l'app Web ContosoWebApp associato al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="85a00-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="85a00-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85a00-112">PARAMETERS</span></span>

### <span data-ttu-id="85a00-113">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="85a00-113">-DestinationSlotName</span></span>
<span data-ttu-id="85a00-114">Nome dello slot di destinazione</span><span class="sxs-lookup"><span data-stu-id="85a00-114">Destination Slot Name</span></span>

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

### <span data-ttu-id="85a00-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="85a00-115">-Name</span></span>
<span data-ttu-id="85a00-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="85a00-116">WebApp Name</span></span>

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

### <span data-ttu-id="85a00-117">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="85a00-117">-PreserveVnet</span></span>
<span data-ttu-id="85a00-118">Mantieni VNET booleano</span><span class="sxs-lookup"><span data-stu-id="85a00-118">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="85a00-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85a00-119">-ResourceGroupName</span></span>
<span data-ttu-id="85a00-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="85a00-120">Resource Group Name</span></span>

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

### <span data-ttu-id="85a00-121">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="85a00-121">-SourceSlotName</span></span>
<span data-ttu-id="85a00-122">Nome dello slot di origine</span><span class="sxs-lookup"><span data-stu-id="85a00-122">Source Slot Name</span></span>

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

### <span data-ttu-id="85a00-123">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="85a00-123">-SwapWithPreviewAction</span></span>
<span data-ttu-id="85a00-124">Scambiare con l'azione anteprima</span><span class="sxs-lookup"><span data-stu-id="85a00-124">Swap With Preview Action</span></span>

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

### <span data-ttu-id="85a00-125">-Web App</span><span class="sxs-lookup"><span data-stu-id="85a00-125">-WebApp</span></span>
<span data-ttu-id="85a00-126">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="85a00-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85a00-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85a00-127">-Confirm</span></span>
<span data-ttu-id="85a00-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85a00-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85a00-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a00-129">-WhatIf</span></span>
<span data-ttu-id="85a00-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85a00-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85a00-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85a00-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85a00-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a00-132">-DefaultProfile</span></span>
<span data-ttu-id="85a00-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85a00-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85a00-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a00-134">CommonParameters</span></span>
<span data-ttu-id="85a00-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85a00-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a00-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85a00-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a00-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85a00-137">INPUTS</span></span>

### <span data-ttu-id="85a00-138">Sito</span><span class="sxs-lookup"><span data-stu-id="85a00-138">Site</span></span>
<span data-ttu-id="85a00-139">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="85a00-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="85a00-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85a00-140">OUTPUTS</span></span>

## <span data-ttu-id="85a00-141">Note</span><span class="sxs-lookup"><span data-stu-id="85a00-141">NOTES</span></span>

## <span data-ttu-id="85a00-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85a00-142">RELATED LINKS</span></span>

