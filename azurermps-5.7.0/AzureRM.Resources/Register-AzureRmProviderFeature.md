---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b41f7cb1c5e3ebec58e3866c94d8e2c62bdf670b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512320"
---
# <span data-ttu-id="15d53-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="15d53-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="15d53-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15d53-102">SYNOPSIS</span></span>
<span data-ttu-id="15d53-103">Registra una caratteristica di provider Azure nell'account.</span><span class="sxs-lookup"><span data-stu-id="15d53-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15d53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15d53-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15d53-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15d53-105">DESCRIPTION</span></span>
<span data-ttu-id="15d53-106">Il cmdlet **Register-AzureRmProviderFeature** registra una caratteristica di Azure provider nell'account.</span><span class="sxs-lookup"><span data-stu-id="15d53-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="15d53-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15d53-107">EXAMPLES</span></span>

### <span data-ttu-id="15d53-108">Esempio 1: registrare una caratteristica</span><span class="sxs-lookup"><span data-stu-id="15d53-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="15d53-109">In questo articolo viene aggiunta la caratteristica AllowApplicationSecurityGroups per Microsoft. Network al proprio account.</span><span class="sxs-lookup"><span data-stu-id="15d53-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="15d53-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15d53-110">PARAMETERS</span></span>

### <span data-ttu-id="15d53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d53-111">-DefaultProfile</span></span>
<span data-ttu-id="15d53-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="15d53-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15d53-113">-Caratteristica</span><span class="sxs-lookup"><span data-stu-id="15d53-113">-FeatureName</span></span>
<span data-ttu-id="15d53-114">Specifica il nome della funzionalità registrata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15d53-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="15d53-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="15d53-115">-ProviderNamespace</span></span>
<span data-ttu-id="15d53-116">Specifica uno spazio dei nomi per cui questo cmdlet registra una caratteristica del provider.</span><span class="sxs-lookup"><span data-stu-id="15d53-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="15d53-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="15d53-117">-Confirm</span></span>
<span data-ttu-id="15d53-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15d53-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15d53-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15d53-119">-WhatIf</span></span>
<span data-ttu-id="15d53-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15d53-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15d53-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15d53-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15d53-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d53-122">CommonParameters</span></span>
<span data-ttu-id="15d53-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15d53-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d53-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15d53-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d53-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15d53-125">INPUTS</span></span>

### <span data-ttu-id="15d53-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="15d53-126">None</span></span>
<span data-ttu-id="15d53-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="15d53-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="15d53-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15d53-128">OUTPUTS</span></span>

### <span data-ttu-id="15d53-129">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="15d53-129">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="15d53-130">Note</span><span class="sxs-lookup"><span data-stu-id="15d53-130">NOTES</span></span>

## <span data-ttu-id="15d53-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15d53-131">RELATED LINKS</span></span>

[<span data-ttu-id="15d53-132">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="15d53-132">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


