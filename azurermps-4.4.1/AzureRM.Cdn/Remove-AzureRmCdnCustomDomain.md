---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 2aa6b3932424f7a8375cca2584a7fc7916124c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519613"
---
# <span data-ttu-id="a0b34-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a0b34-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="a0b34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0b34-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b34-103">Rimuove un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a0b34-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0b34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0b34-104">SYNTAX</span></span>

### <span data-ttu-id="a0b34-105">Parametro set per i parametri dei campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0b34-105">Parameter Set for fields parameters (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0b34-106">Parametro impostato per i parametri degli oggetti</span><span class="sxs-lookup"><span data-stu-id="a0b34-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0b34-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0b34-107">DESCRIPTION</span></span>
<span data-ttu-id="a0b34-108">Il cmdlet **Remove-AzureRmCdnCustomDomain** rimuove il dominio personalizzato da un endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="a0b34-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="a0b34-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0b34-109">EXAMPLES</span></span>

## <span data-ttu-id="a0b34-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0b34-110">PARAMETERS</span></span>

### <span data-ttu-id="a0b34-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a0b34-111">-CdnCustomDomain</span></span>
<span data-ttu-id="a0b34-112">Specifica il dominio personalizzato rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0b34-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0b34-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="a0b34-113">-CustomDomainName</span></span>
<span data-ttu-id="a0b34-114">Specifica il nome della risorsa del dominio personalizzato rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0b34-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b34-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a0b34-115">-EndpointName</span></span>
<span data-ttu-id="a0b34-116">Specifica il nome dell'endpoint da cui questo cmdlet rimuove un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a0b34-116">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b34-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0b34-117">-PassThru</span></span>
<span data-ttu-id="a0b34-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a0b34-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a0b34-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a0b34-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0b34-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a0b34-120">-ProfileName</span></span>
<span data-ttu-id="a0b34-121">Specifica il nome del profilo da cui questo cmdlet rimuove un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a0b34-121">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b34-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0b34-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0b34-123">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a0b34-123">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b34-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0b34-124">-Confirm</span></span>
<span data-ttu-id="a0b34-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0b34-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b34-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0b34-126">-WhatIf</span></span>
<span data-ttu-id="a0b34-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0b34-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0b34-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0b34-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b34-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b34-129">-DefaultProfile</span></span>
<span data-ttu-id="a0b34-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0b34-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0b34-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b34-131">CommonParameters</span></span>
<span data-ttu-id="a0b34-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0b34-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b34-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0b34-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b34-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0b34-134">INPUTS</span></span>

### <span data-ttu-id="a0b34-135">PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a0b34-135">PSCustomDomain</span></span>
<span data-ttu-id="a0b34-136">Il parametro ' CdnCustomDomain ' accetta il valore di tipo ' PSCustomDomain ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a0b34-136">Parameter 'CdnCustomDomain' accepts value of type 'PSCustomDomain' from the pipeline</span></span>

## <span data-ttu-id="a0b34-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0b34-137">OUTPUTS</span></span>

### <span data-ttu-id="a0b34-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0b34-138">System.Boolean</span></span>

## <span data-ttu-id="a0b34-139">Note</span><span class="sxs-lookup"><span data-stu-id="a0b34-139">NOTES</span></span>

## <span data-ttu-id="a0b34-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0b34-140">RELATED LINKS</span></span>

[<span data-ttu-id="a0b34-141">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a0b34-141">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="a0b34-142">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a0b34-142">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="a0b34-143">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a0b34-143">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


