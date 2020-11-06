---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/set-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 33662eed86e5ad7269c81694bc92cd2bf27f93cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509843"
---
# <span data-ttu-id="7b47e-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="7b47e-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="7b47e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b47e-102">SYNOPSIS</span></span>
<span data-ttu-id="7b47e-103">Accettare o rifiutare termini per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="7b47e-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="7b47e-104">Usare Get-AzureRmMarketplaceTerms per ottenere le condizioni per il contratto.</span><span class="sxs-lookup"><span data-stu-id="7b47e-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b47e-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b47e-105">SYNTAX</span></span>

### <span data-ttu-id="7b47e-106">AgreementAcceptParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b47e-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b47e-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b47e-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b47e-108">InputObjectAcceptParametrSet</span><span class="sxs-lookup"><span data-stu-id="7b47e-108">InputObjectAcceptParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b47e-109">InputObjectRejectParametrSet</span><span class="sxs-lookup"><span data-stu-id="7b47e-109">InputObjectRejectParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b47e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b47e-110">DESCRIPTION</span></span>
<span data-ttu-id="7b47e-111">Il cmdlet **set-AzureRmMarketplaceTerms** Salva l'oggetto termini per l'ID di Publisher (Publisher), l'ID offerta (Product) e la tupla ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="7b47e-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="7b47e-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b47e-112">EXAMPLES</span></span>

### <span data-ttu-id="7b47e-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7b47e-113">Example 1</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

### <span data-ttu-id="7b47e-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7b47e-114">Example 2</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

## <span data-ttu-id="7b47e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b47e-115">PARAMETERS</span></span>

### <span data-ttu-id="7b47e-116">-Accettare</span><span class="sxs-lookup"><span data-stu-id="7b47e-116">-Accept</span></span>
<span data-ttu-id="7b47e-117">Passare ad accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="7b47e-117">Pass this to accept the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b47e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b47e-118">-DefaultProfile</span></span>
<span data-ttu-id="7b47e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b47e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b47e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b47e-120">-InputObject</span></span>
<span data-ttu-id="7b47e-121">Oggetto termini restituito nel cmdlet Get-AzureRmMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="7b47e-121">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="7b47e-122">Questo è un parametro obbligatorio se accettato parametro è vero.</span><span class="sxs-lookup"><span data-stu-id="7b47e-122">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b47e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b47e-123">-Name</span></span>
<span data-ttu-id="7b47e-124">Stringa identificatore piano dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="7b47e-124">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b47e-125">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="7b47e-125">-Product</span></span>
<span data-ttu-id="7b47e-126">Offerta identificatore stringa di immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="7b47e-126">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b47e-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="7b47e-127">-Publisher</span></span>
<span data-ttu-id="7b47e-128">Stringa dell'identificatore dell'editore dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="7b47e-128">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b47e-129">-Rifiutare</span><span class="sxs-lookup"><span data-stu-id="7b47e-129">-Reject</span></span>
<span data-ttu-id="7b47e-130">Passare questo articolo per rifiutare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="7b47e-130">Pass this to reject the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b47e-131">-Termini</span><span class="sxs-lookup"><span data-stu-id="7b47e-131">-Terms</span></span>
<span data-ttu-id="7b47e-132">Oggetto termini restituito nel cmdlet Get-AzureRmMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="7b47e-132">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="7b47e-133">Questo è un parametro obbligatorio se accettato parametro è vero.</span><span class="sxs-lookup"><span data-stu-id="7b47e-133">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b47e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b47e-134">-Confirm</span></span>
<span data-ttu-id="7b47e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b47e-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b47e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b47e-136">-WhatIf</span></span>
<span data-ttu-id="7b47e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b47e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b47e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b47e-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b47e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b47e-139">CommonParameters</span></span>
<span data-ttu-id="7b47e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b47e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b47e-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b47e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b47e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b47e-142">INPUTS</span></span>

### <span data-ttu-id="7b47e-143">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="7b47e-143">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="7b47e-144">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="7b47e-144">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="7b47e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b47e-145">OUTPUTS</span></span>

### <span data-ttu-id="7b47e-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="7b47e-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="7b47e-147">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="7b47e-147">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="7b47e-148">Note</span><span class="sxs-lookup"><span data-stu-id="7b47e-148">NOTES</span></span>

## <span data-ttu-id="7b47e-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b47e-149">RELATED LINKS</span></span>

