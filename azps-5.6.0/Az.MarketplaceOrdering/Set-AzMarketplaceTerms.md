---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: b4098481db78bf045abad04aee4e2e5076f71ce1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952333"
---
# <span data-ttu-id="7c46d-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="7c46d-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="7c46d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c46d-102">SYNOPSIS</span></span>
<span data-ttu-id="7c46d-103">Accettare o rifiutare le condizioni per un determinato ID editore (Editore), id offerta(Prodotto) e ID piano(Nome).</span><span class="sxs-lookup"><span data-stu-id="7c46d-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="7c46d-104">Usare le Get-AzMarketplaceTerms per ottenere le condizioni del contratto.</span><span class="sxs-lookup"><span data-stu-id="7c46d-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="7c46d-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c46d-105">SYNTAX</span></span>

### <span data-ttu-id="7c46d-106">AgreementAcceptParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c46d-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c46d-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c46d-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c46d-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c46d-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c46d-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c46d-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c46d-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7c46d-110">DESCRIPTION</span></span>
<span data-ttu-id="7c46d-111">Il cmdlet **Set-AzMarketplaceTerms** salva l'oggetto termini per la tupla ID autore (Publisher), ID offerta(Prodotto) e ID piano(Nome).</span><span class="sxs-lookup"><span data-stu-id="7c46d-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="7c46d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c46d-112">EXAMPLES</span></span>

### <span data-ttu-id="7c46d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c46d-113">Example 1</span></span>
<span data-ttu-id="7c46d-114">Ottieni il contratto per gli editori di Marketplace</span><span class="sxs-lookup"><span data-stu-id="7c46d-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="7c46d-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7c46d-115">Example 2</span></span>
<span data-ttu-id="7c46d-116">Impostare il contratto per l'editore su "Accetta".</span><span class="sxs-lookup"><span data-stu-id="7c46d-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="7c46d-117">Ottenere il valore del parametro 'Terms' dal cmdlet 'Get-AzMarketplaceTerms'</span><span class="sxs-lookup"><span data-stu-id="7c46d-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="7c46d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c46d-118">PARAMETERS</span></span>

### <span data-ttu-id="7c46d-119">-Accetta</span><span class="sxs-lookup"><span data-stu-id="7c46d-119">-Accept</span></span>
<span data-ttu-id="7c46d-120">Accetta questo passaggio per accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="7c46d-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="7c46d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c46d-121">-DefaultProfile</span></span>
<span data-ttu-id="7c46d-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c46d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c46d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c46d-123">-InputObject</span></span>
<span data-ttu-id="7c46d-124">Oggetto Termini restituito nel cmdlet Get-AzMarketplaceTerms termini.</span><span class="sxs-lookup"><span data-stu-id="7c46d-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="7c46d-125">Questo è un parametro obbligatorio se Il parametro Accettato è true.</span><span class="sxs-lookup"><span data-stu-id="7c46d-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="7c46d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7c46d-126">-Name</span></span>
<span data-ttu-id="7c46d-127">Plan identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="7c46d-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="7c46d-128">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="7c46d-128">-Product</span></span>
<span data-ttu-id="7c46d-129">Stringa identificatore dell'offerta dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="7c46d-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="7c46d-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="7c46d-130">-Publisher</span></span>
<span data-ttu-id="7c46d-131">Stringa dell'identificatore dell'editore dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="7c46d-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="7c46d-132">-Rifiuta</span><span class="sxs-lookup"><span data-stu-id="7c46d-132">-Reject</span></span>
<span data-ttu-id="7c46d-133">Passare questo passaggio per rifiutare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="7c46d-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="7c46d-134">-Condizioni</span><span class="sxs-lookup"><span data-stu-id="7c46d-134">-Terms</span></span>
<span data-ttu-id="7c46d-135">Oggetto Termini restituito nel cmdlet Get-AzMarketplaceTerms termini.</span><span class="sxs-lookup"><span data-stu-id="7c46d-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="7c46d-136">Questo è un parametro obbligatorio se Il parametro Accettato è true.</span><span class="sxs-lookup"><span data-stu-id="7c46d-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="7c46d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c46d-137">-Confirm</span></span>
<span data-ttu-id="7c46d-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c46d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c46d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c46d-139">-WhatIf</span></span>
<span data-ttu-id="7c46d-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c46d-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c46d-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c46d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c46d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c46d-142">CommonParameters</span></span>
<span data-ttu-id="7c46d-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c46d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c46d-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c46d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c46d-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="7c46d-145">INPUTS</span></span>

### <span data-ttu-id="7c46d-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="7c46d-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="7c46d-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c46d-147">OUTPUTS</span></span>

### <span data-ttu-id="7c46d-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="7c46d-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="7c46d-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="7c46d-149">NOTES</span></span>

## <span data-ttu-id="7c46d-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c46d-150">RELATED LINKS</span></span>
