---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329875"
---
# <span data-ttu-id="76984-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="76984-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="76984-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76984-102">SYNOPSIS</span></span>
<span data-ttu-id="76984-103">Rimuovere un'offerta dall'archivio privato.</span><span class="sxs-lookup"><span data-stu-id="76984-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="76984-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76984-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76984-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76984-105">DESCRIPTION</span></span>
<span data-ttu-id="76984-106">Rimuovere un'offerta da un archivio privato creato in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="76984-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="76984-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76984-107">EXAMPLES</span></span>

### <span data-ttu-id="76984-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="76984-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="76984-109">Rimuovere un'offerta da un archivio privato creato in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="76984-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="76984-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76984-110">PARAMETERS</span></span>

### <span data-ttu-id="76984-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76984-111">-DefaultProfile</span></span>
<span data-ttu-id="76984-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76984-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76984-113">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="76984-113">-OfferId</span></span>
<span data-ttu-id="76984-114">Offerta privateStore di Azure Marketplace necessaria</span><span class="sxs-lookup"><span data-stu-id="76984-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="76984-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76984-115">-PassThru</span></span>
<span data-ttu-id="76984-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="76984-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="76984-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="76984-117">-PrivateStoreId</span></span>
<span data-ttu-id="76984-118">PrivateStore di Azure Marketplace obbligatorio</span><span class="sxs-lookup"><span data-stu-id="76984-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="76984-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="76984-119">-Confirm</span></span>
<span data-ttu-id="76984-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76984-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76984-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76984-121">-WhatIf</span></span>
<span data-ttu-id="76984-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76984-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76984-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76984-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76984-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76984-124">CommonParameters</span></span>
<span data-ttu-id="76984-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76984-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76984-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76984-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76984-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76984-127">INPUTS</span></span>

### <span data-ttu-id="76984-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="76984-128">None</span></span>

## <span data-ttu-id="76984-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76984-129">OUTPUTS</span></span>

### <span data-ttu-id="76984-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76984-130">System.Boolean</span></span>

## <span data-ttu-id="76984-131">Note</span><span class="sxs-lookup"><span data-stu-id="76984-131">NOTES</span></span>

## <span data-ttu-id="76984-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76984-132">RELATED LINKS</span></span>
