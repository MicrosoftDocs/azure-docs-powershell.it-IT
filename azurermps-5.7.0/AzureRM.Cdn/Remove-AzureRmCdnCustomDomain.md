---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 8c6e3629d4ac6e8592370393b94727234a6eb12a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510047"
---
# <span data-ttu-id="78772-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78772-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="78772-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78772-102">SYNOPSIS</span></span>
<span data-ttu-id="78772-103">Rimuove un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="78772-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78772-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78772-104">SYNTAX</span></span>

### <span data-ttu-id="78772-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78772-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78772-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78772-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78772-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78772-107">DESCRIPTION</span></span>
<span data-ttu-id="78772-108">Il cmdlet **Remove-AzureRmCdnCustomDomain** rimuove il dominio personalizzato da un endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="78772-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="78772-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78772-109">EXAMPLES</span></span>

## <span data-ttu-id="78772-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78772-110">PARAMETERS</span></span>

### <span data-ttu-id="78772-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78772-111">-CdnCustomDomain</span></span>
<span data-ttu-id="78772-112">Specifica il dominio personalizzato rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78772-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78772-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="78772-113">-CustomDomainName</span></span>
<span data-ttu-id="78772-114">Specifica il nome della risorsa del dominio personalizzato rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78772-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78772-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78772-115">-DefaultProfile</span></span>
<span data-ttu-id="78772-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="78772-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78772-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="78772-117">-EndpointName</span></span>
<span data-ttu-id="78772-118">Specifica il nome dell'endpoint da cui questo cmdlet rimuove un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="78772-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78772-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78772-119">-PassThru</span></span>
<span data-ttu-id="78772-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="78772-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="78772-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="78772-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78772-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="78772-122">-ProfileName</span></span>
<span data-ttu-id="78772-123">Specifica il nome del profilo da cui questo cmdlet rimuove un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="78772-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78772-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78772-124">-ResourceGroupName</span></span>
<span data-ttu-id="78772-125">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="78772-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78772-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="78772-126">-Confirm</span></span>
<span data-ttu-id="78772-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78772-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78772-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78772-128">-WhatIf</span></span>
<span data-ttu-id="78772-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78772-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78772-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78772-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78772-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78772-131">CommonParameters</span></span>
<span data-ttu-id="78772-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78772-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78772-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78772-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78772-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78772-134">INPUTS</span></span>

### <span data-ttu-id="78772-135">PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78772-135">PSCustomDomain</span></span>
<span data-ttu-id="78772-136">Il parametro ' CdnCustomDomain ' accetta il valore di tipo ' PSCustomDomain ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="78772-136">Parameter 'CdnCustomDomain' accepts value of type 'PSCustomDomain' from the pipeline</span></span>

## <span data-ttu-id="78772-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78772-137">OUTPUTS</span></span>

### <span data-ttu-id="78772-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78772-138">System.Boolean</span></span>

## <span data-ttu-id="78772-139">Note</span><span class="sxs-lookup"><span data-stu-id="78772-139">NOTES</span></span>

## <span data-ttu-id="78772-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78772-140">RELATED LINKS</span></span>

[<span data-ttu-id="78772-141">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78772-141">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="78772-142">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78772-142">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="78772-143">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78772-143">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


