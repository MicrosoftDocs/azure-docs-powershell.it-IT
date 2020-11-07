---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: 1cea045bd9b663e542bb435003df79f153542a75
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835195"
---
# <span data-ttu-id="86c7f-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="86c7f-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="86c7f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="86c7f-103">Accettare o rifiutare termini per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="86c7f-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="86c7f-104">Usare Get-AzMarketplaceTerms per ottenere le condizioni per il contratto.</span><span class="sxs-lookup"><span data-stu-id="86c7f-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="86c7f-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86c7f-105">SYNTAX</span></span>

### <span data-ttu-id="86c7f-106">AgreementAcceptParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86c7f-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86c7f-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86c7f-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86c7f-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="86c7f-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c7f-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86c7f-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c7f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86c7f-110">DESCRIPTION</span></span>
<span data-ttu-id="86c7f-111">Il cmdlet **set-AzMarketplaceTerms** Salva l'oggetto termini per l'ID di Publisher (Publisher), l'ID offerta (Product) e la tupla ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="86c7f-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="86c7f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86c7f-112">EXAMPLES</span></span>

### <span data-ttu-id="86c7f-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86c7f-113">Example 1</span></span>
<span data-ttu-id="86c7f-114">Ottenere il contratto Marketplace Publisher</span><span class="sxs-lookup"><span data-stu-id="86c7f-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="86c7f-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="86c7f-115">Example 2</span></span>
<span data-ttu-id="86c7f-116">Impostare il contratto di Publisher su "accetta".</span><span class="sxs-lookup"><span data-stu-id="86c7f-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="86c7f-117">Ottenere il valore per il parametro "termini" dal cmdlet "Get-AzMarketplaceTerms"</span><span class="sxs-lookup"><span data-stu-id="86c7f-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="86c7f-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86c7f-118">PARAMETERS</span></span>

### <span data-ttu-id="86c7f-119">-Accettare</span><span class="sxs-lookup"><span data-stu-id="86c7f-119">-Accept</span></span>
<span data-ttu-id="86c7f-120">Passare ad accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="86c7f-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="86c7f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c7f-121">-DefaultProfile</span></span>
<span data-ttu-id="86c7f-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86c7f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86c7f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86c7f-123">-InputObject</span></span>
<span data-ttu-id="86c7f-124">Oggetto termini restituito nel cmdlet Get-AzMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="86c7f-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="86c7f-125">Questo è un parametro obbligatorio se accettato parametro è vero.</span><span class="sxs-lookup"><span data-stu-id="86c7f-125">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="86c7f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="86c7f-126">-Name</span></span>
<span data-ttu-id="86c7f-127">Stringa identificatore piano dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="86c7f-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="86c7f-128">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="86c7f-128">-Product</span></span>
<span data-ttu-id="86c7f-129">Offerta identificatore stringa di immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="86c7f-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="86c7f-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="86c7f-130">-Publisher</span></span>
<span data-ttu-id="86c7f-131">Stringa dell'identificatore dell'editore dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="86c7f-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="86c7f-132">-Rifiutare</span><span class="sxs-lookup"><span data-stu-id="86c7f-132">-Reject</span></span>
<span data-ttu-id="86c7f-133">Passare questo articolo per rifiutare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="86c7f-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="86c7f-134">-Termini</span><span class="sxs-lookup"><span data-stu-id="86c7f-134">-Terms</span></span>
<span data-ttu-id="86c7f-135">Oggetto termini restituito nel cmdlet Get-AzMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="86c7f-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="86c7f-136">Questo è un parametro obbligatorio se accettato parametro è vero.</span><span class="sxs-lookup"><span data-stu-id="86c7f-136">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="86c7f-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="86c7f-137">-Confirm</span></span>
<span data-ttu-id="86c7f-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86c7f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c7f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c7f-139">-WhatIf</span></span>
<span data-ttu-id="86c7f-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86c7f-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86c7f-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86c7f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c7f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c7f-142">CommonParameters</span></span>
<span data-ttu-id="86c7f-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c7f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c7f-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c7f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c7f-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86c7f-145">INPUTS</span></span>

### <span data-ttu-id="86c7f-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="86c7f-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="86c7f-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86c7f-147">OUTPUTS</span></span>

### <span data-ttu-id="86c7f-148">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="86c7f-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="86c7f-149">Note</span><span class="sxs-lookup"><span data-stu-id="86c7f-149">NOTES</span></span>

## <span data-ttu-id="86c7f-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86c7f-150">RELATED LINKS</span></span>
