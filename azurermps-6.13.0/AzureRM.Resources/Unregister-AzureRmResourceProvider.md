---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
ms.openlocfilehash: d957859fc03a5d8beec90190d473240acb7b2482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687754"
---
# <span data-ttu-id="4360b-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4360b-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="4360b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4360b-102">SYNOPSIS</span></span>
<span data-ttu-id="4360b-103">Annulla la registrazione di un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="4360b-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4360b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4360b-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4360b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4360b-105">DESCRIPTION</span></span>
<span data-ttu-id="4360b-106">Il cmdlet **Unregister-AzureRmResourceProvider** Annulla la registrazione di un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="4360b-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="4360b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4360b-107">EXAMPLES</span></span>

## <span data-ttu-id="4360b-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4360b-108">PARAMETERS</span></span>

### <span data-ttu-id="4360b-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4360b-109">-ApiVersion</span></span>
<span data-ttu-id="4360b-110">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="4360b-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4360b-111">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4360b-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4360b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4360b-112">-DefaultProfile</span></span>
<span data-ttu-id="4360b-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4360b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4360b-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="4360b-114">-Pre</span></span>
<span data-ttu-id="4360b-115">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="4360b-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4360b-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="4360b-116">-ProviderNamespace</span></span>
<span data-ttu-id="4360b-117">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="4360b-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="4360b-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4360b-118">-Confirm</span></span>
<span data-ttu-id="4360b-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4360b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4360b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4360b-120">-WhatIf</span></span>
<span data-ttu-id="4360b-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4360b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4360b-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4360b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4360b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4360b-123">CommonParameters</span></span>
<span data-ttu-id="4360b-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4360b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4360b-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4360b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4360b-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4360b-126">INPUTS</span></span>

## <span data-ttu-id="4360b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4360b-127">OUTPUTS</span></span>

## <span data-ttu-id="4360b-128">Note</span><span class="sxs-lookup"><span data-stu-id="4360b-128">NOTES</span></span>

## <span data-ttu-id="4360b-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4360b-129">RELATED LINKS</span></span>

[<span data-ttu-id="4360b-130">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4360b-130">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="4360b-131">Registro-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4360b-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

