---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
ms.openlocfilehash: 6c17b3732cf5eab46f5826896dacafd3639aa788
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020802"
---
# <span data-ttu-id="4cb74-101">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4cb74-101">New-AzCdnProfile</span></span>

## <span data-ttu-id="4cb74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4cb74-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb74-103">Crea un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="4cb74-103">Creates a CDN profile.</span></span>

## <span data-ttu-id="4cb74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cb74-104">SYNTAX</span></span>

```
New-AzCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cb74-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cb74-105">DESCRIPTION</span></span>
<span data-ttu-id="4cb74-106">Il cmdlet **New-AzCdnProfile** crea un profilo CDN (Azure Content delivering Network).</span><span class="sxs-lookup"><span data-stu-id="4cb74-106">The **New-AzCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="4cb74-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cb74-107">EXAMPLES</span></span>

## <span data-ttu-id="4cb74-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4cb74-108">PARAMETERS</span></span>

### <span data-ttu-id="4cb74-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb74-109">-DefaultProfile</span></span>
<span data-ttu-id="4cb74-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4cb74-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cb74-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4cb74-111">-Location</span></span>
<span data-ttu-id="4cb74-112">Specifica la posizione della risorsa del profilo.</span><span class="sxs-lookup"><span data-stu-id="4cb74-112">Specifies the resource location of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb74-113">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4cb74-113">-ProfileName</span></span>
<span data-ttu-id="4cb74-114">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="4cb74-114">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cb74-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cb74-115">-ResourceGroupName</span></span>
<span data-ttu-id="4cb74-116">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="4cb74-116">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cb74-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="4cb74-117">-Sku</span></span>
<span data-ttu-id="4cb74-118">Specifica l'USK del profilo.</span><span class="sxs-lookup"><span data-stu-id="4cb74-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn, Standard_Microsoft

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb74-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="4cb74-119">-Tag</span></span>
<span data-ttu-id="4cb74-120">Tag da associare al profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="4cb74-120">The tags to associate with the Azure CDN profile.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb74-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4cb74-121">-Confirm</span></span>
<span data-ttu-id="4cb74-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cb74-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cb74-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cb74-123">-WhatIf</span></span>
<span data-ttu-id="4cb74-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cb74-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cb74-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cb74-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cb74-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb74-126">CommonParameters</span></span>
<span data-ttu-id="4cb74-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cb74-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb74-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cb74-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb74-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4cb74-129">INPUTS</span></span>

### <span data-ttu-id="4cb74-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4cb74-130">System.String</span></span>

## <span data-ttu-id="4cb74-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cb74-131">OUTPUTS</span></span>

### <span data-ttu-id="4cb74-132">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="4cb74-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="4cb74-133">Note</span><span class="sxs-lookup"><span data-stu-id="4cb74-133">NOTES</span></span>

## <span data-ttu-id="4cb74-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cb74-134">RELATED LINKS</span></span>

[<span data-ttu-id="4cb74-135">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4cb74-135">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="4cb74-136">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4cb74-136">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="4cb74-137">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4cb74-137">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


