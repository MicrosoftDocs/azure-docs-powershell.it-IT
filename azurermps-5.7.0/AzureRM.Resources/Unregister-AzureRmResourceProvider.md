---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
ms.openlocfilehash: 875dd42cb0aefd6d6422d99463cd56ace720411a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686682"
---
# <span data-ttu-id="5433e-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5433e-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="5433e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5433e-102">SYNOPSIS</span></span>
<span data-ttu-id="5433e-103">Annulla la registrazione di un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="5433e-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5433e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5433e-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5433e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5433e-105">DESCRIPTION</span></span>
<span data-ttu-id="5433e-106">Il cmdlet **Unregister-AzureRmResourceProvider** Annulla la registrazione di un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="5433e-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="5433e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5433e-107">EXAMPLES</span></span>

## <span data-ttu-id="5433e-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5433e-108">PARAMETERS</span></span>

### <span data-ttu-id="5433e-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5433e-109">-ApiVersion</span></span>
<span data-ttu-id="5433e-110">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="5433e-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5433e-111">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5433e-111">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5433e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5433e-112">-DefaultProfile</span></span>
<span data-ttu-id="5433e-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5433e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5433e-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="5433e-114">-Pre</span></span>
<span data-ttu-id="5433e-115">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="5433e-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5433e-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="5433e-116">-ProviderNamespace</span></span>
<span data-ttu-id="5433e-117">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="5433e-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="5433e-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5433e-118">-Confirm</span></span>
<span data-ttu-id="5433e-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5433e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5433e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5433e-120">-WhatIf</span></span>
<span data-ttu-id="5433e-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5433e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5433e-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5433e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5433e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5433e-123">CommonParameters</span></span>
<span data-ttu-id="5433e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5433e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5433e-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5433e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5433e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5433e-126">INPUTS</span></span>

### <span data-ttu-id="5433e-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5433e-127">None</span></span>
<span data-ttu-id="5433e-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5433e-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5433e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5433e-129">OUTPUTS</span></span>

### <span data-ttu-id="5433e-130">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider]</span><span class="sxs-lookup"><span data-stu-id="5433e-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider]</span></span>

## <span data-ttu-id="5433e-131">Note</span><span class="sxs-lookup"><span data-stu-id="5433e-131">NOTES</span></span>

## <span data-ttu-id="5433e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5433e-132">RELATED LINKS</span></span>

[<span data-ttu-id="5433e-133">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5433e-133">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="5433e-134">Registro-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5433e-134">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


