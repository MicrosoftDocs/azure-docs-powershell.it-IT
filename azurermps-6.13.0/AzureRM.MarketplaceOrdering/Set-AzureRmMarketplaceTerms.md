---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/set-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 7932a733fcd672d8ee92e6452765745281ee0a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685706"
---
# <span data-ttu-id="4f408-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="4f408-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="4f408-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f408-102">SYNOPSIS</span></span>
<span data-ttu-id="4f408-103">Accettare o rifiutare termini per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="4f408-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="4f408-104">Usare Get-AzureRmMarketplaceTerms per ottenere le condizioni per il contratto.</span><span class="sxs-lookup"><span data-stu-id="4f408-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f408-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f408-105">SYNTAX</span></span>

### <span data-ttu-id="4f408-106">AgreementAcceptParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4f408-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f408-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f408-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f408-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f408-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f408-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f408-109">InputObjectRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f408-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f408-110">DESCRIPTION</span></span>
<span data-ttu-id="4f408-111">Il cmdlet **set-AzureRmMarketplaceTerms** Salva l'oggetto termini per l'ID di Publisher (Publisher), l'ID offerta (Product) e la tupla ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="4f408-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="4f408-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f408-112">EXAMPLES</span></span>

### <span data-ttu-id="4f408-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4f408-113">Example 1</span></span>
<span data-ttu-id="4f408-114">Ottenere il contratto Marketplace Publisher</span><span class="sxs-lookup"><span data-stu-id="4f408-114">Get the marketplace publisher agreement</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

### <span data-ttu-id="4f408-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4f408-115">Example 2</span></span>
<span data-ttu-id="4f408-116">Impostare il contratto di Publisher su "accetta".</span><span class="sxs-lookup"><span data-stu-id="4f408-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="4f408-117">Ottenere il valore per il parametro "termini" dal cmdlet "Get-AzureRmMarketplaceTerms"</span><span class="sxs-lookup"><span data-stu-id="4f408-117">Get the value for the 'Terms' parameter from the 'Get-AzureRmMarketplaceTerms' cmdlet</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```


## <span data-ttu-id="4f408-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f408-118">PARAMETERS</span></span>

### <span data-ttu-id="4f408-119">-Accettare</span><span class="sxs-lookup"><span data-stu-id="4f408-119">-Accept</span></span>
<span data-ttu-id="4f408-120">Passare ad accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="4f408-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f408-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f408-121">-DefaultProfile</span></span>
<span data-ttu-id="4f408-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f408-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f408-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f408-123">-InputObject</span></span>
<span data-ttu-id="4f408-124">Oggetto termini restituito nel cmdlet Get-AzureRmMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="4f408-124">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="4f408-125">Questo è un parametro obbligatorio se accettato parametro è vero.</span><span class="sxs-lookup"><span data-stu-id="4f408-125">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f408-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f408-126">-Name</span></span>
<span data-ttu-id="4f408-127">Stringa identificatore piano dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="4f408-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="4f408-128">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="4f408-128">-Product</span></span>
<span data-ttu-id="4f408-129">Offerta identificatore stringa di immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="4f408-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="4f408-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4f408-130">-Publisher</span></span>
<span data-ttu-id="4f408-131">Stringa dell'identificatore dell'editore dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="4f408-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="4f408-132">-Rifiutare</span><span class="sxs-lookup"><span data-stu-id="4f408-132">-Reject</span></span>
<span data-ttu-id="4f408-133">Passare questo articolo per rifiutare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="4f408-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f408-134">-Termini</span><span class="sxs-lookup"><span data-stu-id="4f408-134">-Terms</span></span>
<span data-ttu-id="4f408-135">Oggetto termini restituito nel cmdlet Get-AzureRmMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="4f408-135">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="4f408-136">Questo è un parametro obbligatorio se accettato parametro è vero.</span><span class="sxs-lookup"><span data-stu-id="4f408-136">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="4f408-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4f408-137">-Confirm</span></span>
<span data-ttu-id="4f408-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f408-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f408-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f408-139">-WhatIf</span></span>
<span data-ttu-id="4f408-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f408-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f408-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f408-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f408-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f408-142">CommonParameters</span></span>
<span data-ttu-id="4f408-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f408-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f408-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f408-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f408-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f408-145">INPUTS</span></span>

### <span data-ttu-id="4f408-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="4f408-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="4f408-147">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4f408-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4f408-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f408-148">OUTPUTS</span></span>

### <span data-ttu-id="4f408-149">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="4f408-149">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="4f408-150">Note</span><span class="sxs-lookup"><span data-stu-id="4f408-150">NOTES</span></span>

## <span data-ttu-id="4f408-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f408-151">RELATED LINKS</span></span>
