---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: c64f84c9f41dba29e54b14a69235bccd764ea750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686932"
---
# <span data-ttu-id="03be4-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="03be4-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="03be4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03be4-102">SYNOPSIS</span></span>
<span data-ttu-id="03be4-103">Crea un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="03be4-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03be4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03be4-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03be4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03be4-105">DESCRIPTION</span></span>
<span data-ttu-id="03be4-106">Il cmdlet **New-AzureRmCdnProfile** crea un profilo CDN (Azure Content delivering Network).</span><span class="sxs-lookup"><span data-stu-id="03be4-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="03be4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03be4-107">EXAMPLES</span></span>

## <span data-ttu-id="03be4-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03be4-108">PARAMETERS</span></span>

### <span data-ttu-id="03be4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03be4-109">-DefaultProfile</span></span>
<span data-ttu-id="03be4-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="03be4-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03be4-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="03be4-111">-Location</span></span>
<span data-ttu-id="03be4-112">Specifica la posizione della risorsa del profilo.</span><span class="sxs-lookup"><span data-stu-id="03be4-112">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="03be4-113">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="03be4-113">-ProfileName</span></span>
<span data-ttu-id="03be4-114">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="03be4-114">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="03be4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03be4-115">-ResourceGroupName</span></span>
<span data-ttu-id="03be4-116">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="03be4-116">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="03be4-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="03be4-117">-Sku</span></span>
<span data-ttu-id="03be4-118">Specifica l'USK del profilo.</span><span class="sxs-lookup"><span data-stu-id="03be4-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03be4-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="03be4-119">-Tag</span></span>
<span data-ttu-id="03be4-120">Tag da associare al profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="03be4-120">The tags to associate with the Azure CDN profile.</span></span>

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

### <span data-ttu-id="03be4-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="03be4-121">-Confirm</span></span>
<span data-ttu-id="03be4-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03be4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03be4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03be4-123">-WhatIf</span></span>
<span data-ttu-id="03be4-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03be4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03be4-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03be4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03be4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03be4-126">CommonParameters</span></span>
<span data-ttu-id="03be4-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03be4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03be4-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03be4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03be4-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03be4-129">INPUTS</span></span>

### <span data-ttu-id="03be4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="03be4-130">System.String</span></span>

## <span data-ttu-id="03be4-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03be4-131">OUTPUTS</span></span>

### <span data-ttu-id="03be4-132">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="03be4-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="03be4-133">Note</span><span class="sxs-lookup"><span data-stu-id="03be4-133">NOTES</span></span>

## <span data-ttu-id="03be4-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03be4-134">RELATED LINKS</span></span>

[<span data-ttu-id="03be4-135">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="03be4-135">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="03be4-136">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="03be4-136">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="03be4-137">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="03be4-137">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


