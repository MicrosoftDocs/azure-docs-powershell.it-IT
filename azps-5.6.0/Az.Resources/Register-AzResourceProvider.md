---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 8fe856b1b8b710c1db139474f15d432f32c2652a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982253"
---
# <span data-ttu-id="ad7eb-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ad7eb-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="ad7eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad7eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ad7eb-103">Registra un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad7eb-103">Registers a resource provider.</span></span>

## <span data-ttu-id="ad7eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad7eb-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad7eb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ad7eb-105">DESCRIPTION</span></span>
<span data-ttu-id="ad7eb-106">Il cmdlet **Register-AzResourceProvider** registra un provider di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="ad7eb-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="ad7eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad7eb-107">EXAMPLES</span></span>

### <span data-ttu-id="ad7eb-108">Esempio 1: Registrare un provider</span><span class="sxs-lookup"><span data-stu-id="ad7eb-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="ad7eb-109">Il provider di rete Microsoft.Network viene registrato per l'account.</span><span class="sxs-lookup"><span data-stu-id="ad7eb-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="ad7eb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad7eb-110">PARAMETERS</span></span>

### <span data-ttu-id="ad7eb-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ad7eb-111">-ApiVersion</span></span>
<span data-ttu-id="ad7eb-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad7eb-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ad7eb-113">È possibile specificare una versione diversa da quella predefinita.</span><span class="sxs-lookup"><span data-stu-id="ad7eb-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad7eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad7eb-114">-DefaultProfile</span></span>
<span data-ttu-id="ad7eb-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ad7eb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad7eb-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="ad7eb-116">-Pre</span></span>
<span data-ttu-id="ad7eb-117">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="ad7eb-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad7eb-118">-Provider Provider Provider</span><span class="sxs-lookup"><span data-stu-id="ad7eb-118">-ProviderNamespace</span></span>
<span data-ttu-id="ad7eb-119">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad7eb-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="ad7eb-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad7eb-120">-Confirm</span></span>
<span data-ttu-id="ad7eb-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad7eb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad7eb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad7eb-122">-WhatIf</span></span>
<span data-ttu-id="ad7eb-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad7eb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad7eb-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad7eb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad7eb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad7eb-125">CommonParameters</span></span>
<span data-ttu-id="ad7eb-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad7eb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad7eb-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ad7eb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad7eb-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="ad7eb-128">INPUTS</span></span>

### <span data-ttu-id="ad7eb-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ad7eb-129">System.String</span></span>

## <span data-ttu-id="ad7eb-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad7eb-130">OUTPUTS</span></span>

### <span data-ttu-id="ad7eb-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ad7eb-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="ad7eb-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="ad7eb-132">NOTES</span></span>

## <span data-ttu-id="ad7eb-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad7eb-133">RELATED LINKS</span></span>

[<span data-ttu-id="ad7eb-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ad7eb-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="ad7eb-135">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ad7eb-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


