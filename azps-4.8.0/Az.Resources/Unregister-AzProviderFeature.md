---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: 6cb27f66871038fa1849671391e1d7d9f8f3ccd7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188873"
---
# <span data-ttu-id="ca29c-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="ca29c-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="ca29c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca29c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca29c-103">Annulla la registrazione di una caratteristica di Azure provider nell'account.</span><span class="sxs-lookup"><span data-stu-id="ca29c-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="ca29c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca29c-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca29c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca29c-105">DESCRIPTION</span></span>
<span data-ttu-id="ca29c-106">Il cmdlet **Unregister-AzProviderFeature** Annulla la registrazione di una caratteristica del provider Azure nell'account.</span><span class="sxs-lookup"><span data-stu-id="ca29c-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="ca29c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca29c-107">EXAMPLES</span></span>

### <span data-ttu-id="ca29c-108">Esempio 1: annullare la registrazione di una caratteristica</span><span class="sxs-lookup"><span data-stu-id="ca29c-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="ca29c-109">Questa operazione Annulla la registrazione della funzionalità AllowApplicationSecurityGroups per Microsoft. Network dall'account.</span><span class="sxs-lookup"><span data-stu-id="ca29c-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="ca29c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca29c-110">PARAMETERS</span></span>

### <span data-ttu-id="ca29c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca29c-111">-DefaultProfile</span></span>
<span data-ttu-id="ca29c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca29c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca29c-113">-Caratteristica</span><span class="sxs-lookup"><span data-stu-id="ca29c-113">-FeatureName</span></span>
<span data-ttu-id="ca29c-114">Nome della caratteristica.</span><span class="sxs-lookup"><span data-stu-id="ca29c-114">The feature name.</span></span>

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

### <span data-ttu-id="ca29c-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="ca29c-115">-ProviderNamespace</span></span>
<span data-ttu-id="ca29c-116">Spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca29c-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="ca29c-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca29c-117">-Confirm</span></span>
<span data-ttu-id="ca29c-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca29c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca29c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca29c-119">-WhatIf</span></span>
<span data-ttu-id="ca29c-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca29c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca29c-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca29c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca29c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca29c-122">CommonParameters</span></span>
<span data-ttu-id="ca29c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca29c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca29c-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca29c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca29c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca29c-125">INPUTS</span></span>

### <span data-ttu-id="ca29c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ca29c-126">System.String</span></span>

## <span data-ttu-id="ca29c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca29c-127">OUTPUTS</span></span>

### <span data-ttu-id="ca29c-128">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="ca29c-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="ca29c-129">Note</span><span class="sxs-lookup"><span data-stu-id="ca29c-129">NOTES</span></span>

## <span data-ttu-id="ca29c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca29c-130">RELATED LINKS</span></span>
