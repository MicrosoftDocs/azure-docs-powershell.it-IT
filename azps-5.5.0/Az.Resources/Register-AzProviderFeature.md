---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 35cb8ad956419a2fcbfe427ce23e518986da63ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208435"
---
# <span data-ttu-id="4806a-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="4806a-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="4806a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4806a-102">SYNOPSIS</span></span>
<span data-ttu-id="4806a-103">Registra una funzionalità del provider di Azure nel tuo account.</span><span class="sxs-lookup"><span data-stu-id="4806a-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="4806a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4806a-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4806a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4806a-105">DESCRIPTION</span></span>
<span data-ttu-id="4806a-106">Il cmdlet **Register-AzProviderFeature** registra una caratteristica del provider di Azure nell'account.</span><span class="sxs-lookup"><span data-stu-id="4806a-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="4806a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4806a-107">EXAMPLES</span></span>

### <span data-ttu-id="4806a-108">Esempio 1: Registrare una caratteristica</span><span class="sxs-lookup"><span data-stu-id="4806a-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="4806a-109">All'account verrà aggiunta la caratteristica AllowApplicationSecurityGroups per Microsoft.Network.</span><span class="sxs-lookup"><span data-stu-id="4806a-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="4806a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4806a-110">PARAMETERS</span></span>

### <span data-ttu-id="4806a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4806a-111">-DefaultProfile</span></span>
<span data-ttu-id="4806a-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4806a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4806a-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="4806a-113">-FeatureName</span></span>
<span data-ttu-id="4806a-114">Specifica il nome della caratteristica che questo cmdlet registra.</span><span class="sxs-lookup"><span data-stu-id="4806a-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="4806a-115">-Provider Provider</span><span class="sxs-lookup"><span data-stu-id="4806a-115">-ProviderNamespace</span></span>
<span data-ttu-id="4806a-116">Specifica uno spazio dei nomi per il quale questo cmdlet registra una caratteristica del provider.</span><span class="sxs-lookup"><span data-stu-id="4806a-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="4806a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4806a-117">-Confirm</span></span>
<span data-ttu-id="4806a-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4806a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4806a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4806a-119">-WhatIf</span></span>
<span data-ttu-id="4806a-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4806a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4806a-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4806a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4806a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4806a-122">CommonParameters</span></span>
<span data-ttu-id="4806a-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4806a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4806a-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4806a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4806a-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="4806a-125">INPUTS</span></span>

### <span data-ttu-id="4806a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4806a-126">System.String</span></span>

## <span data-ttu-id="4806a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4806a-127">OUTPUTS</span></span>

### <span data-ttu-id="4806a-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="4806a-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="4806a-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="4806a-129">NOTES</span></span>

## <span data-ttu-id="4806a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4806a-130">RELATED LINKS</span></span>

[<span data-ttu-id="4806a-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="4806a-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


