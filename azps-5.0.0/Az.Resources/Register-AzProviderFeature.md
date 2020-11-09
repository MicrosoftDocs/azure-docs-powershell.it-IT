---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 35cb8ad956419a2fcbfe427ce23e518986da63ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311100"
---
# <span data-ttu-id="b7493-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="b7493-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="b7493-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7493-102">SYNOPSIS</span></span>
<span data-ttu-id="b7493-103">Registra una caratteristica di provider Azure nell'account.</span><span class="sxs-lookup"><span data-stu-id="b7493-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="b7493-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7493-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7493-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7493-105">DESCRIPTION</span></span>
<span data-ttu-id="b7493-106">Il cmdlet **Register-AzProviderFeature** registra una caratteristica di Azure provider nell'account.</span><span class="sxs-lookup"><span data-stu-id="b7493-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="b7493-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7493-107">EXAMPLES</span></span>

### <span data-ttu-id="b7493-108">Esempio 1: registrare una caratteristica</span><span class="sxs-lookup"><span data-stu-id="b7493-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="b7493-109">In questo articolo viene aggiunta la caratteristica AllowApplicationSecurityGroups per Microsoft. Network al proprio account.</span><span class="sxs-lookup"><span data-stu-id="b7493-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="b7493-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7493-110">PARAMETERS</span></span>

### <span data-ttu-id="b7493-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7493-111">-DefaultProfile</span></span>
<span data-ttu-id="b7493-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b7493-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7493-113">-Caratteristica</span><span class="sxs-lookup"><span data-stu-id="b7493-113">-FeatureName</span></span>
<span data-ttu-id="b7493-114">Specifica il nome della funzionalità registrata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7493-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="b7493-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="b7493-115">-ProviderNamespace</span></span>
<span data-ttu-id="b7493-116">Specifica uno spazio dei nomi per cui questo cmdlet registra una caratteristica del provider.</span><span class="sxs-lookup"><span data-stu-id="b7493-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="b7493-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b7493-117">-Confirm</span></span>
<span data-ttu-id="b7493-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7493-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7493-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7493-119">-WhatIf</span></span>
<span data-ttu-id="b7493-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7493-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7493-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7493-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7493-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7493-122">CommonParameters</span></span>
<span data-ttu-id="b7493-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7493-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7493-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7493-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7493-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7493-125">INPUTS</span></span>

### <span data-ttu-id="b7493-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b7493-126">System.String</span></span>

## <span data-ttu-id="b7493-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7493-127">OUTPUTS</span></span>

### <span data-ttu-id="b7493-128">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="b7493-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="b7493-129">Note</span><span class="sxs-lookup"><span data-stu-id="b7493-129">NOTES</span></span>

## <span data-ttu-id="b7493-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7493-130">RELATED LINKS</span></span>

[<span data-ttu-id="b7493-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="b7493-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


