---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 829f6b4e95e1d45d68f12ed6dbd8ad7c7987eba3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003758"
---
# <span data-ttu-id="77835-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="77835-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="77835-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77835-102">SYNOPSIS</span></span>
<span data-ttu-id="77835-103">Rimuovi un'offerta dall'archivio privato.</span><span class="sxs-lookup"><span data-stu-id="77835-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="77835-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77835-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77835-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="77835-105">DESCRIPTION</span></span>
<span data-ttu-id="77835-106">Rimuovere dall'archivio privato un'offerta creata nell'ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="77835-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="77835-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77835-107">EXAMPLES</span></span>

### <span data-ttu-id="77835-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="77835-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="77835-109">Rimuovere dall'archivio privato un'offerta creata nell'ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="77835-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="77835-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77835-110">PARAMETERS</span></span>

### <span data-ttu-id="77835-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77835-111">-DefaultProfile</span></span>
<span data-ttu-id="77835-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77835-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77835-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="77835-113">-OfferId</span></span>
<span data-ttu-id="77835-114">Offerta di Azure Marketplace privata obbligatoria</span><span class="sxs-lookup"><span data-stu-id="77835-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="77835-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77835-115">-PassThru</span></span>
<span data-ttu-id="77835-116">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="77835-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="77835-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="77835-117">-PrivateStoreId</span></span>
<span data-ttu-id="77835-118">Archivio privato Azure Marketplace obbligatorio</span><span class="sxs-lookup"><span data-stu-id="77835-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="77835-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77835-119">-Confirm</span></span>
<span data-ttu-id="77835-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77835-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77835-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77835-121">-WhatIf</span></span>
<span data-ttu-id="77835-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77835-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77835-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77835-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77835-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77835-124">CommonParameters</span></span>
<span data-ttu-id="77835-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77835-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77835-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="77835-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77835-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="77835-127">INPUTS</span></span>

### <span data-ttu-id="77835-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="77835-128">None</span></span>

## <span data-ttu-id="77835-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77835-129">OUTPUTS</span></span>

### <span data-ttu-id="77835-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77835-130">System.Boolean</span></span>

## <span data-ttu-id="77835-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="77835-131">NOTES</span></span>

## <span data-ttu-id="77835-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77835-132">RELATED LINKS</span></span>
