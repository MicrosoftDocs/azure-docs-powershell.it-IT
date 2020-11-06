---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 843bb68c5aebc18af60e1cc74915b269738059f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521605"
---
# <span data-ttu-id="d6a48-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="d6a48-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="d6a48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6a48-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a48-103">Accettare o rifiutare termini per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="d6a48-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="d6a48-104">Usare Get-AzureRmMarketplaceTerms per ottenere le condizioni per il contratto.</span><span class="sxs-lookup"><span data-stu-id="d6a48-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6a48-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6a48-105">SYNTAX</span></span>

### <span data-ttu-id="d6a48-106">AgreementAcceptParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d6a48-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6a48-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6a48-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6a48-108">InputObjectAcceptParametrSet</span><span class="sxs-lookup"><span data-stu-id="d6a48-108">InputObjectAcceptParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6a48-109">InputObjectRejectParametrSet</span><span class="sxs-lookup"><span data-stu-id="d6a48-109">InputObjectRejectParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6a48-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6a48-110">DESCRIPTION</span></span>
<span data-ttu-id="d6a48-111">Il cmdlet **set-AzureRmMarketplaceTerms** Salva l'oggetto termini per l'ID di Publisher (Publisher), l'ID offerta (Product) e la tupla ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="d6a48-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="d6a48-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6a48-112">EXAMPLES</span></span>

### <span data-ttu-id="d6a48-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d6a48-113">Example 1</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

### <span data-ttu-id="d6a48-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d6a48-114">Example 2</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

## <span data-ttu-id="d6a48-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6a48-115">PARAMETERS</span></span>

### <span data-ttu-id="d6a48-116">-Accettare</span><span class="sxs-lookup"><span data-stu-id="d6a48-116">-Accept</span></span>
<span data-ttu-id="d6a48-117">Passare ad accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="d6a48-117">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="d6a48-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a48-118">-DefaultProfile</span></span>
<span data-ttu-id="d6a48-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6a48-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6a48-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6a48-120">-InputObject</span></span>
<span data-ttu-id="d6a48-121">Oggetto termini restituito nel cmdlet Get-AzureRmMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="d6a48-121">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="d6a48-122">Questo è un parametro obbligatorio se accettato parametro è vero.</span><span class="sxs-lookup"><span data-stu-id="d6a48-122">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="d6a48-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6a48-123">-Name</span></span>
<span data-ttu-id="d6a48-124">Stringa identificatore piano dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="d6a48-124">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="d6a48-125">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="d6a48-125">-Product</span></span>
<span data-ttu-id="d6a48-126">Offerta identificatore stringa di immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="d6a48-126">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="d6a48-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d6a48-127">-Publisher</span></span>
<span data-ttu-id="d6a48-128">Stringa dell'identificatore dell'editore dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="d6a48-128">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="d6a48-129">-Rifiutare</span><span class="sxs-lookup"><span data-stu-id="d6a48-129">-Reject</span></span>
<span data-ttu-id="d6a48-130">Passare questo articolo per rifiutare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="d6a48-130">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="d6a48-131">-Termini</span><span class="sxs-lookup"><span data-stu-id="d6a48-131">-Terms</span></span>
<span data-ttu-id="d6a48-132">Oggetto termini restituito nel cmdlet Get-AzureRmMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="d6a48-132">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="d6a48-133">Questo è un parametro obbligatorio se accettato parametro è vero.</span><span class="sxs-lookup"><span data-stu-id="d6a48-133">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="d6a48-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d6a48-134">-Confirm</span></span>
<span data-ttu-id="d6a48-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6a48-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6a48-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6a48-136">-WhatIf</span></span>
<span data-ttu-id="d6a48-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6a48-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6a48-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6a48-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6a48-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a48-139">CommonParameters</span></span>
<span data-ttu-id="d6a48-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6a48-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a48-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6a48-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a48-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6a48-142">INPUTS</span></span>

### <span data-ttu-id="d6a48-143">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="d6a48-143">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="d6a48-144">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="d6a48-144">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="d6a48-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6a48-145">OUTPUTS</span></span>

### <span data-ttu-id="d6a48-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="d6a48-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="d6a48-147">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="d6a48-147">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="d6a48-148">Note</span><span class="sxs-lookup"><span data-stu-id="d6a48-148">NOTES</span></span>

## <span data-ttu-id="d6a48-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6a48-149">RELATED LINKS</span></span>

