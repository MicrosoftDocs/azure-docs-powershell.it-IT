---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019654"
---
# <span data-ttu-id="a924d-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a924d-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="a924d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a924d-102">SYNOPSIS</span></span>
<span data-ttu-id="a924d-103">Annulla la registrazione di un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="a924d-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="a924d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a924d-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a924d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a924d-105">DESCRIPTION</span></span>
<span data-ttu-id="a924d-106">Il cmdlet **Unregister-AzResourceProvider** Annulla la registrazione di un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="a924d-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="a924d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a924d-107">EXAMPLES</span></span>

### <span data-ttu-id="a924d-108">Esempio 1: annullamento della registrazione del provider di risorse con ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="a924d-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="a924d-109">Questo comando Annulla la registrazione del provider di risorse "Microsoft. support".</span><span class="sxs-lookup"><span data-stu-id="a924d-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="a924d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a924d-110">PARAMETERS</span></span>

### <span data-ttu-id="a924d-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a924d-111">-ApiVersion</span></span>
<span data-ttu-id="a924d-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="a924d-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a924d-113">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a924d-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="a924d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a924d-114">-DefaultProfile</span></span>
<span data-ttu-id="a924d-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a924d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a924d-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="a924d-116">-Pre</span></span>
<span data-ttu-id="a924d-117">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a924d-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a924d-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="a924d-118">-ProviderNamespace</span></span>
<span data-ttu-id="a924d-119">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="a924d-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="a924d-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a924d-120">-Confirm</span></span>
<span data-ttu-id="a924d-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a924d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a924d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a924d-122">-WhatIf</span></span>
<span data-ttu-id="a924d-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a924d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a924d-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a924d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a924d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a924d-125">CommonParameters</span></span>
<span data-ttu-id="a924d-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a924d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a924d-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a924d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a924d-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a924d-128">INPUTS</span></span>

### <span data-ttu-id="a924d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a924d-129">System.String</span></span>

## <span data-ttu-id="a924d-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a924d-130">OUTPUTS</span></span>

### <span data-ttu-id="a924d-131">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a924d-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="a924d-132">Note</span><span class="sxs-lookup"><span data-stu-id="a924d-132">NOTES</span></span>

## <span data-ttu-id="a924d-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a924d-133">RELATED LINKS</span></span>

[<span data-ttu-id="a924d-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a924d-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="a924d-135">Registro-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a924d-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


