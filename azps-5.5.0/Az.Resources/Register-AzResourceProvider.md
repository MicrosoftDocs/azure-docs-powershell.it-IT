---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 45b8bc67529556e9a9d53bd3280c6475f0e60df1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208427"
---
# <span data-ttu-id="21a83-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="21a83-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="21a83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21a83-102">SYNOPSIS</span></span>
<span data-ttu-id="21a83-103">Registra un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="21a83-103">Registers a resource provider.</span></span>

## <span data-ttu-id="21a83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21a83-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21a83-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="21a83-105">DESCRIPTION</span></span>
<span data-ttu-id="21a83-106">Il cmdlet **Register-AzResourceProvider** registra un provider di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="21a83-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="21a83-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21a83-107">EXAMPLES</span></span>

### <span data-ttu-id="21a83-108">Esempio 1: Registrare un provider</span><span class="sxs-lookup"><span data-stu-id="21a83-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="21a83-109">In questo modo il provider di microsoft.network viene registrato per l'account.</span><span class="sxs-lookup"><span data-stu-id="21a83-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="21a83-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21a83-110">PARAMETERS</span></span>

### <span data-ttu-id="21a83-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="21a83-111">-ApiVersion</span></span>
<span data-ttu-id="21a83-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="21a83-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="21a83-113">È possibile specificare una versione diversa da quella predefinita.</span><span class="sxs-lookup"><span data-stu-id="21a83-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="21a83-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a83-114">-DefaultProfile</span></span>
<span data-ttu-id="21a83-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="21a83-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21a83-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="21a83-116">-Pre</span></span>
<span data-ttu-id="21a83-117">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="21a83-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="21a83-118">-Provider Provider</span><span class="sxs-lookup"><span data-stu-id="21a83-118">-ProviderNamespace</span></span>
<span data-ttu-id="21a83-119">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="21a83-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="21a83-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21a83-120">-Confirm</span></span>
<span data-ttu-id="21a83-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21a83-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21a83-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21a83-122">-WhatIf</span></span>
<span data-ttu-id="21a83-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21a83-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21a83-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21a83-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21a83-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a83-125">CommonParameters</span></span>
<span data-ttu-id="21a83-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a83-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a83-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21a83-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a83-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="21a83-128">INPUTS</span></span>

### <span data-ttu-id="21a83-129">System.String</span><span class="sxs-lookup"><span data-stu-id="21a83-129">System.String</span></span>

## <span data-ttu-id="21a83-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21a83-130">OUTPUTS</span></span>

### <span data-ttu-id="21a83-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="21a83-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="21a83-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="21a83-132">NOTES</span></span>

## <span data-ttu-id="21a83-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21a83-133">RELATED LINKS</span></span>

[<span data-ttu-id="21a83-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="21a83-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="21a83-135">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="21a83-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


