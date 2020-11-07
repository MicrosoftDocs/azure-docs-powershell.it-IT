---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: ffab8a1ab23d21835eb913c03a952c4c4839a559
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673869"
---
# <span data-ttu-id="3a8ee-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="3a8ee-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="3a8ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="3a8ee-103">Accettare o rifiutare termini per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="3a8ee-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="3a8ee-104">Usare Get-AzMarketplaceTerms per ottenere le condizioni per il contratto.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="3a8ee-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a8ee-105">SYNTAX</span></span>

### <span data-ttu-id="3a8ee-106">AgreementAcceptParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3a8ee-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a8ee-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a8ee-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a8ee-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a8ee-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8ee-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a8ee-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a8ee-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a8ee-110">DESCRIPTION</span></span>
<span data-ttu-id="3a8ee-111">Il cmdlet **set-AzMarketplaceTerms** Salva l'oggetto termini per l'ID di Publisher (Publisher), l'ID offerta (Product) e la tupla ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="3a8ee-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="3a8ee-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a8ee-112">EXAMPLES</span></span>

### <span data-ttu-id="3a8ee-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3a8ee-113">Example 1</span></span>
<span data-ttu-id="3a8ee-114">Ottenere il contratto Marketplace Publisher</span><span class="sxs-lookup"><span data-stu-id="3a8ee-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="3a8ee-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3a8ee-115">Example 2</span></span>
<span data-ttu-id="3a8ee-116">Impostare il contratto di Publisher su "accetta".</span><span class="sxs-lookup"><span data-stu-id="3a8ee-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="3a8ee-117">Ottenere il valore per il parametro "termini" dal cmdlet "Get-AzMarketplaceTerms"</span><span class="sxs-lookup"><span data-stu-id="3a8ee-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="3a8ee-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a8ee-118">PARAMETERS</span></span>

### <span data-ttu-id="3a8ee-119">-Accettare</span><span class="sxs-lookup"><span data-stu-id="3a8ee-119">-Accept</span></span>
<span data-ttu-id="3a8ee-120">Passare ad accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="3a8ee-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a8ee-121">-DefaultProfile</span></span>
<span data-ttu-id="3a8ee-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a8ee-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a8ee-123">-InputObject</span></span>
<span data-ttu-id="3a8ee-124">Oggetto termini restituito nel cmdlet Get-AzMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="3a8ee-125">Si tratta di un parametro obbligatorio se il parametro accepted è true.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="3a8ee-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a8ee-126">-Name</span></span>
<span data-ttu-id="3a8ee-127">Stringa identificatore piano dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="3a8ee-128">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="3a8ee-128">-Product</span></span>
<span data-ttu-id="3a8ee-129">Offerta identificatore stringa di immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="3a8ee-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3a8ee-130">-Publisher</span></span>
<span data-ttu-id="3a8ee-131">Stringa dell'identificatore dell'editore dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="3a8ee-132">-Rifiutare</span><span class="sxs-lookup"><span data-stu-id="3a8ee-132">-Reject</span></span>
<span data-ttu-id="3a8ee-133">Passare questo articolo per rifiutare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="3a8ee-134">-Termini</span><span class="sxs-lookup"><span data-stu-id="3a8ee-134">-Terms</span></span>
<span data-ttu-id="3a8ee-135">Oggetto termini restituito nel cmdlet Get-AzMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="3a8ee-136">Si tratta di un parametro obbligatorio se il parametro accepted è true.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="3a8ee-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3a8ee-137">-Confirm</span></span>
<span data-ttu-id="3a8ee-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a8ee-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a8ee-139">-WhatIf</span></span>
<span data-ttu-id="3a8ee-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a8ee-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a8ee-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a8ee-142">CommonParameters</span></span>
<span data-ttu-id="3a8ee-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a8ee-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a8ee-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a8ee-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a8ee-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a8ee-145">INPUTS</span></span>

### <span data-ttu-id="3a8ee-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="3a8ee-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="3a8ee-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a8ee-147">OUTPUTS</span></span>

### <span data-ttu-id="3a8ee-148">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="3a8ee-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="3a8ee-149">Note</span><span class="sxs-lookup"><span data-stu-id="3a8ee-149">NOTES</span></span>

## <span data-ttu-id="3a8ee-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a8ee-150">RELATED LINKS</span></span>
