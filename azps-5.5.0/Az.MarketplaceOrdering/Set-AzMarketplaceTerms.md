---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: fb40d1c103da1cc9f1cfe306ebdaab5abf6ec316
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180255"
---
# <span data-ttu-id="66a0b-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="66a0b-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="66a0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="66a0b-103">Accettare o rifiutare le condizioni per un determinato ID editore (Editore), id offerta(Prodotto) e ID piano(Nome).</span><span class="sxs-lookup"><span data-stu-id="66a0b-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="66a0b-104">Utilizza il Get-AzMarketplaceTerms per ottenere le condizioni del contratto.</span><span class="sxs-lookup"><span data-stu-id="66a0b-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="66a0b-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66a0b-105">SYNTAX</span></span>

### <span data-ttu-id="66a0b-106">AgreementAcceptParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="66a0b-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66a0b-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66a0b-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66a0b-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="66a0b-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66a0b-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66a0b-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66a0b-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="66a0b-110">DESCRIPTION</span></span>
<span data-ttu-id="66a0b-111">Il cmdlet **Set-AzMarketplaceTerms** salva l'oggetto termini per la tupla ID autore (Publisher), ID offerta(Prodotto) e ID piano(Nome).</span><span class="sxs-lookup"><span data-stu-id="66a0b-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="66a0b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66a0b-112">EXAMPLES</span></span>

### <span data-ttu-id="66a0b-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="66a0b-113">Example 1</span></span>
<span data-ttu-id="66a0b-114">Ottieni il contratto per gli editori di Marketplace</span><span class="sxs-lookup"><span data-stu-id="66a0b-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="66a0b-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="66a0b-115">Example 2</span></span>
<span data-ttu-id="66a0b-116">Impostare il contratto per l'editore su "Accetta".</span><span class="sxs-lookup"><span data-stu-id="66a0b-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="66a0b-117">Ottenere il valore del parametro 'Terms' dal cmdlet 'Get-AzMarketplaceTerms'</span><span class="sxs-lookup"><span data-stu-id="66a0b-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="66a0b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66a0b-118">PARAMETERS</span></span>

### <span data-ttu-id="66a0b-119">-Accetta</span><span class="sxs-lookup"><span data-stu-id="66a0b-119">-Accept</span></span>
<span data-ttu-id="66a0b-120">Accetta questo passaggio per accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="66a0b-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="66a0b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a0b-121">-DefaultProfile</span></span>
<span data-ttu-id="66a0b-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66a0b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66a0b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66a0b-123">-InputObject</span></span>
<span data-ttu-id="66a0b-124">Oggetto Termini restituito nel cmdlet Get-AzMarketplaceTerms termini.</span><span class="sxs-lookup"><span data-stu-id="66a0b-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="66a0b-125">Questo è un parametro obbligatorio se Il parametro Accettato è true.</span><span class="sxs-lookup"><span data-stu-id="66a0b-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="66a0b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="66a0b-126">-Name</span></span>
<span data-ttu-id="66a0b-127">Stringa identificatore del piano per la distribuzione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="66a0b-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="66a0b-128">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="66a0b-128">-Product</span></span>
<span data-ttu-id="66a0b-129">Stringa identificatore dell'offerta dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="66a0b-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="66a0b-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="66a0b-130">-Publisher</span></span>
<span data-ttu-id="66a0b-131">Stringa dell'identificatore dell'editore dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="66a0b-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="66a0b-132">-Rifiuta</span><span class="sxs-lookup"><span data-stu-id="66a0b-132">-Reject</span></span>
<span data-ttu-id="66a0b-133">Passare questo passaggio per rifiutare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="66a0b-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="66a0b-134">-Condizioni</span><span class="sxs-lookup"><span data-stu-id="66a0b-134">-Terms</span></span>
<span data-ttu-id="66a0b-135">Oggetto Termini restituito nel cmdlet Get-AzMarketplaceTerms termini.</span><span class="sxs-lookup"><span data-stu-id="66a0b-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="66a0b-136">Questo è un parametro obbligatorio se Il parametro Accettato è true.</span><span class="sxs-lookup"><span data-stu-id="66a0b-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="66a0b-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66a0b-137">-Confirm</span></span>
<span data-ttu-id="66a0b-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66a0b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66a0b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a0b-139">-WhatIf</span></span>
<span data-ttu-id="66a0b-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66a0b-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66a0b-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66a0b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66a0b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a0b-142">CommonParameters</span></span>
<span data-ttu-id="66a0b-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a0b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a0b-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a0b-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a0b-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="66a0b-145">INPUTS</span></span>

### <span data-ttu-id="66a0b-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="66a0b-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="66a0b-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66a0b-147">OUTPUTS</span></span>

### <span data-ttu-id="66a0b-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="66a0b-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="66a0b-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="66a0b-149">NOTES</span></span>

## <span data-ttu-id="66a0b-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66a0b-150">RELATED LINKS</span></span>
