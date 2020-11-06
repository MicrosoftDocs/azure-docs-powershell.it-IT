---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b519108918f2c26d86807302314a4defed1a0050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519528"
---
# <span data-ttu-id="72125-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="72125-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="72125-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72125-102">SYNOPSIS</span></span>
<span data-ttu-id="72125-103">Registra una caratteristica di provider Azure nell'account.</span><span class="sxs-lookup"><span data-stu-id="72125-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72125-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72125-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72125-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72125-105">DESCRIPTION</span></span>
<span data-ttu-id="72125-106">Il cmdlet **Register-AzureRmProviderFeature** registra una caratteristica di Azure provider nell'account.</span><span class="sxs-lookup"><span data-stu-id="72125-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="72125-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72125-107">EXAMPLES</span></span>

## <span data-ttu-id="72125-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72125-108">PARAMETERS</span></span>

### <span data-ttu-id="72125-109">-Caratteristica</span><span class="sxs-lookup"><span data-stu-id="72125-109">-FeatureName</span></span>
<span data-ttu-id="72125-110">Specifica il nome della funzionalità registrata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72125-110">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="72125-111">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="72125-111">-ProviderNamespace</span></span>
<span data-ttu-id="72125-112">Specifica uno spazio dei nomi per cui questo cmdlet registra una caratteristica del provider.</span><span class="sxs-lookup"><span data-stu-id="72125-112">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="72125-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72125-113">-Confirm</span></span>
<span data-ttu-id="72125-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72125-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72125-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72125-115">-WhatIf</span></span>
<span data-ttu-id="72125-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72125-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72125-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72125-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72125-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72125-118">-DefaultProfile</span></span>
<span data-ttu-id="72125-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72125-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72125-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72125-120">CommonParameters</span></span>
<span data-ttu-id="72125-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72125-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72125-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72125-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72125-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72125-123">INPUTS</span></span>

## <span data-ttu-id="72125-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72125-124">OUTPUTS</span></span>

### <span data-ttu-id="72125-125">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="72125-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="72125-126">Note</span><span class="sxs-lookup"><span data-stu-id="72125-126">NOTES</span></span>

## <span data-ttu-id="72125-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72125-127">RELATED LINKS</span></span>

[<span data-ttu-id="72125-128">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="72125-128">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


