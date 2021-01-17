---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476109"
---
# <span data-ttu-id="c1b98-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="c1b98-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="c1b98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1b98-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b98-103">Rimuovere un'offerta dall'archivio privato.</span><span class="sxs-lookup"><span data-stu-id="c1b98-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="c1b98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1b98-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1b98-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1b98-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b98-106">Rimuovere un'offerta da un archivio privato creato in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="c1b98-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="c1b98-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1b98-107">EXAMPLES</span></span>

### <span data-ttu-id="c1b98-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c1b98-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="c1b98-109">Rimuovere un'offerta da un archivio privato creato in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="c1b98-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="c1b98-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1b98-110">PARAMETERS</span></span>

### <span data-ttu-id="c1b98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b98-111">-DefaultProfile</span></span>
<span data-ttu-id="c1b98-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b98-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1b98-113">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="c1b98-113">-OfferId</span></span>
<span data-ttu-id="c1b98-114">Offerta privateStore di Azure Marketplace necessaria</span><span class="sxs-lookup"><span data-stu-id="c1b98-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="c1b98-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1b98-115">-PassThru</span></span>
<span data-ttu-id="c1b98-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c1b98-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c1b98-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="c1b98-117">-PrivateStoreId</span></span>
<span data-ttu-id="c1b98-118">PrivateStore di Azure Marketplace obbligatorio</span><span class="sxs-lookup"><span data-stu-id="c1b98-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="c1b98-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c1b98-119">-Confirm</span></span>
<span data-ttu-id="c1b98-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1b98-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1b98-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1b98-121">-WhatIf</span></span>
<span data-ttu-id="c1b98-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1b98-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1b98-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1b98-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1b98-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b98-124">CommonParameters</span></span>
<span data-ttu-id="c1b98-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b98-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b98-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1b98-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b98-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1b98-127">INPUTS</span></span>

### <span data-ttu-id="c1b98-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c1b98-128">None</span></span>

## <span data-ttu-id="c1b98-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1b98-129">OUTPUTS</span></span>

### <span data-ttu-id="c1b98-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1b98-130">System.Boolean</span></span>

## <span data-ttu-id="c1b98-131">Note</span><span class="sxs-lookup"><span data-stu-id="c1b98-131">NOTES</span></span>

## <span data-ttu-id="c1b98-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1b98-132">RELATED LINKS</span></span>
