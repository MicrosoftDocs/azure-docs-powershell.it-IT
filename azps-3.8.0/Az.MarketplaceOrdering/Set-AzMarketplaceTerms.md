---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: fb40d1c103da1cc9f1cfe306ebdaab5abf6ec316
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022501"
---
# <span data-ttu-id="85c24-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="85c24-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="85c24-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85c24-102">SYNOPSIS</span></span>
<span data-ttu-id="85c24-103">Accettare o rifiutare termini per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="85c24-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="85c24-104">Usare Get-AzMarketplaceTerms per ottenere le condizioni per il contratto.</span><span class="sxs-lookup"><span data-stu-id="85c24-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="85c24-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85c24-105">SYNTAX</span></span>

### <span data-ttu-id="85c24-106">AgreementAcceptParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85c24-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85c24-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c24-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85c24-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c24-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85c24-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c24-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85c24-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85c24-110">DESCRIPTION</span></span>
<span data-ttu-id="85c24-111">Il cmdlet **set-AzMarketplaceTerms** Salva l'oggetto termini per l'ID di Publisher (Publisher), l'ID offerta (Product) e la tupla ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="85c24-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="85c24-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85c24-112">EXAMPLES</span></span>

### <span data-ttu-id="85c24-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="85c24-113">Example 1</span></span>
<span data-ttu-id="85c24-114">Ottenere il contratto Marketplace Publisher</span><span class="sxs-lookup"><span data-stu-id="85c24-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="85c24-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="85c24-115">Example 2</span></span>
<span data-ttu-id="85c24-116">Impostare il contratto di Publisher su "accetta".</span><span class="sxs-lookup"><span data-stu-id="85c24-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="85c24-117">Ottenere il valore per il parametro "termini" dal cmdlet "Get-AzMarketplaceTerms"</span><span class="sxs-lookup"><span data-stu-id="85c24-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="85c24-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85c24-118">PARAMETERS</span></span>

### <span data-ttu-id="85c24-119">-Accettare</span><span class="sxs-lookup"><span data-stu-id="85c24-119">-Accept</span></span>
<span data-ttu-id="85c24-120">Passare ad accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="85c24-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c24-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c24-121">-DefaultProfile</span></span>
<span data-ttu-id="85c24-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85c24-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85c24-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85c24-123">-InputObject</span></span>
<span data-ttu-id="85c24-124">Oggetto termini restituito nel cmdlet Get-AzMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="85c24-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="85c24-125">Si tratta di un parametro obbligatorio se il parametro accepted è true.</span><span class="sxs-lookup"><span data-stu-id="85c24-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85c24-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="85c24-126">-Name</span></span>
<span data-ttu-id="85c24-127">Stringa identificatore piano dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="85c24-127">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c24-128">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="85c24-128">-Product</span></span>
<span data-ttu-id="85c24-129">Offerta identificatore stringa di immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="85c24-129">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c24-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="85c24-130">-Publisher</span></span>
<span data-ttu-id="85c24-131">Stringa dell'identificatore dell'editore dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="85c24-131">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c24-132">-Rifiutare</span><span class="sxs-lookup"><span data-stu-id="85c24-132">-Reject</span></span>
<span data-ttu-id="85c24-133">Passare questo articolo per rifiutare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="85c24-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c24-134">-Termini</span><span class="sxs-lookup"><span data-stu-id="85c24-134">-Terms</span></span>
<span data-ttu-id="85c24-135">Oggetto termini restituito nel cmdlet Get-AzMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="85c24-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="85c24-136">Si tratta di un parametro obbligatorio se il parametro accepted è true.</span><span class="sxs-lookup"><span data-stu-id="85c24-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c24-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85c24-137">-Confirm</span></span>
<span data-ttu-id="85c24-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85c24-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85c24-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85c24-139">-WhatIf</span></span>
<span data-ttu-id="85c24-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85c24-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85c24-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85c24-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85c24-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c24-142">CommonParameters</span></span>
<span data-ttu-id="85c24-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c24-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c24-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85c24-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c24-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85c24-145">INPUTS</span></span>

### <span data-ttu-id="85c24-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="85c24-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="85c24-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85c24-147">OUTPUTS</span></span>

### <span data-ttu-id="85c24-148">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="85c24-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="85c24-149">Note</span><span class="sxs-lookup"><span data-stu-id="85c24-149">NOTES</span></span>

## <span data-ttu-id="85c24-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85c24-150">RELATED LINKS</span></span>
