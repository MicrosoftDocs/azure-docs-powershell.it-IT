---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178695"
---
# <span data-ttu-id="1d975-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="1d975-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="1d975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d975-102">SYNOPSIS</span></span>
<span data-ttu-id="1d975-103">Annulla la registrazione di una funzionalità del provider Azure nel tuo account.</span><span class="sxs-lookup"><span data-stu-id="1d975-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="1d975-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d975-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d975-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1d975-105">DESCRIPTION</span></span>
<span data-ttu-id="1d975-106">Il cmdlet **Unregister-AzProviderFeature** annulla la registrazione di una funzionalità del provider di Azure nel tuo account.</span><span class="sxs-lookup"><span data-stu-id="1d975-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="1d975-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d975-107">EXAMPLES</span></span>

### <span data-ttu-id="1d975-108">Esempio 1: Annullare la registrazione di una funzionalità</span><span class="sxs-lookup"><span data-stu-id="1d975-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="1d975-109">Questa operazione annulla la registrazione della funzionalità AllowApplicationSecurityGroups per Microsoft.Network dall'account.</span><span class="sxs-lookup"><span data-stu-id="1d975-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="1d975-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d975-110">PARAMETERS</span></span>

### <span data-ttu-id="1d975-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d975-111">-DefaultProfile</span></span>
<span data-ttu-id="1d975-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d975-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d975-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="1d975-113">-FeatureName</span></span>
<span data-ttu-id="1d975-114">Nome della caratteristica.</span><span class="sxs-lookup"><span data-stu-id="1d975-114">The feature name.</span></span>

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

### <span data-ttu-id="1d975-115">-Provider Provider</span><span class="sxs-lookup"><span data-stu-id="1d975-115">-ProviderNamespace</span></span>
<span data-ttu-id="1d975-116">Spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="1d975-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="1d975-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d975-117">-Confirm</span></span>
<span data-ttu-id="1d975-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d975-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d975-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d975-119">-WhatIf</span></span>
<span data-ttu-id="1d975-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d975-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d975-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d975-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d975-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d975-122">CommonParameters</span></span>
<span data-ttu-id="1d975-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d975-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d975-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d975-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d975-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="1d975-125">INPUTS</span></span>

### <span data-ttu-id="1d975-126">System.String</span><span class="sxs-lookup"><span data-stu-id="1d975-126">System.String</span></span>

## <span data-ttu-id="1d975-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d975-127">OUTPUTS</span></span>

### <span data-ttu-id="1d975-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="1d975-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="1d975-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="1d975-129">NOTES</span></span>

## <span data-ttu-id="1d975-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d975-130">RELATED LINKS</span></span>