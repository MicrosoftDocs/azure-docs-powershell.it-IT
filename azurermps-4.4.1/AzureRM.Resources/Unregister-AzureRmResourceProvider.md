---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
ms.openlocfilehash: 686e6902c7653f4a820f51b02b134a51963bb532
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686155"
---
# <span data-ttu-id="c84b9-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c84b9-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="c84b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c84b9-102">SYNOPSIS</span></span>
<span data-ttu-id="c84b9-103">Annulla la registrazione di un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="c84b9-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c84b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c84b9-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c84b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c84b9-105">DESCRIPTION</span></span>
<span data-ttu-id="c84b9-106">Il cmdlet **Unregister-AzureRmResourceProvider** Annulla la registrazione di un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="c84b9-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="c84b9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c84b9-107">EXAMPLES</span></span>

## <span data-ttu-id="c84b9-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c84b9-108">PARAMETERS</span></span>

### <span data-ttu-id="c84b9-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c84b9-109">-ApiVersion</span></span>
<span data-ttu-id="c84b9-110">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="c84b9-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c84b9-111">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c84b9-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="c84b9-112">-Pre</span><span class="sxs-lookup"><span data-stu-id="c84b9-112">-Pre</span></span>
<span data-ttu-id="c84b9-113">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="c84b9-113">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c84b9-114">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c84b9-114">-ProviderNamespace</span></span>
<span data-ttu-id="c84b9-115">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="c84b9-115">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="c84b9-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c84b9-116">-Confirm</span></span>
<span data-ttu-id="c84b9-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c84b9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c84b9-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c84b9-118">-WhatIf</span></span>
<span data-ttu-id="c84b9-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c84b9-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c84b9-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c84b9-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c84b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c84b9-121">-DefaultProfile</span></span>
<span data-ttu-id="c84b9-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c84b9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c84b9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c84b9-123">CommonParameters</span></span>
<span data-ttu-id="c84b9-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c84b9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c84b9-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c84b9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c84b9-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c84b9-126">INPUTS</span></span>

## <span data-ttu-id="c84b9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c84b9-127">OUTPUTS</span></span>

### <span data-ttu-id="c84b9-128">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider]</span><span class="sxs-lookup"><span data-stu-id="c84b9-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider]</span></span>

## <span data-ttu-id="c84b9-129">Note</span><span class="sxs-lookup"><span data-stu-id="c84b9-129">NOTES</span></span>

## <span data-ttu-id="c84b9-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c84b9-130">RELATED LINKS</span></span>

[<span data-ttu-id="c84b9-131">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c84b9-131">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="c84b9-132">Registro-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c84b9-132">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


