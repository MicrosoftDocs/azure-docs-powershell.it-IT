---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: 5423844d7f466a827f3a452a05cf3999236198d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510059"
---
# <span data-ttu-id="34116-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="34116-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="34116-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34116-102">SYNOPSIS</span></span>
<span data-ttu-id="34116-103">Crea un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="34116-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34116-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34116-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34116-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34116-105">DESCRIPTION</span></span>
<span data-ttu-id="34116-106">Il cmdlet **New-AzureRmCdnProfile** crea un profilo CDN (Azure Content delivering Network).</span><span class="sxs-lookup"><span data-stu-id="34116-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="34116-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34116-107">EXAMPLES</span></span>

## <span data-ttu-id="34116-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34116-108">PARAMETERS</span></span>

### <span data-ttu-id="34116-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34116-109">-DefaultProfile</span></span>
<span data-ttu-id="34116-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="34116-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34116-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="34116-111">-Location</span></span>
<span data-ttu-id="34116-112">Specifica la posizione della risorsa del profilo.</span><span class="sxs-lookup"><span data-stu-id="34116-112">Specifies the resource location of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34116-113">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="34116-113">-ProfileName</span></span>
<span data-ttu-id="34116-114">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="34116-114">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34116-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34116-115">-ResourceGroupName</span></span>
<span data-ttu-id="34116-116">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="34116-116">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34116-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="34116-117">-Sku</span></span>
<span data-ttu-id="34116-118">Specifica l'USK del profilo.</span><span class="sxs-lookup"><span data-stu-id="34116-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34116-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="34116-119">-Tag</span></span>
<span data-ttu-id="34116-120">Tag da associare al profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="34116-120">The tags to associate with the Azure CDN profile.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34116-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="34116-121">-Confirm</span></span>
<span data-ttu-id="34116-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34116-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34116-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34116-123">-WhatIf</span></span>
<span data-ttu-id="34116-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34116-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34116-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34116-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34116-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34116-126">CommonParameters</span></span>
<span data-ttu-id="34116-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34116-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34116-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34116-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34116-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34116-129">INPUTS</span></span>

### <span data-ttu-id="34116-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="34116-130">None</span></span>
<span data-ttu-id="34116-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="34116-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34116-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34116-132">OUTPUTS</span></span>

### <span data-ttu-id="34116-133">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="34116-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="34116-134">Note</span><span class="sxs-lookup"><span data-stu-id="34116-134">NOTES</span></span>

## <span data-ttu-id="34116-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34116-135">RELATED LINKS</span></span>

[<span data-ttu-id="34116-136">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="34116-136">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="34116-137">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="34116-137">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="34116-138">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="34116-138">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


