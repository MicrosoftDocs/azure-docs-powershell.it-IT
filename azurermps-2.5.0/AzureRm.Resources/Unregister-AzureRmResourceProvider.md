---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ead0edddccc5372c04e2e4b77d7860bbad29c27a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866196"
---
# <span data-ttu-id="4e4bd-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4e4bd-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="4e4bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e4bd-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4bd-103">Annulla la registrazione di un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e4bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e4bd-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e4bd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e4bd-105">DESCRIPTION</span></span>
<span data-ttu-id="4e4bd-106">Il cmdlet **Unregister-AzureRmResourceProvider** Annulla la registrazione di un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="4e4bd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e4bd-107">EXAMPLES</span></span>

## <span data-ttu-id="4e4bd-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e4bd-108">PARAMETERS</span></span>

### <span data-ttu-id="4e4bd-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4e4bd-109">-ApiVersion</span></span>
<span data-ttu-id="4e4bd-110">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4e4bd-111">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4e4bd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4bd-112">-DefaultProfile</span></span>
<span data-ttu-id="4e4bd-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4e4bd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e4bd-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="4e4bd-114">-Pre</span></span>
<span data-ttu-id="4e4bd-115">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4e4bd-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="4e4bd-116">-ProviderNamespace</span></span>
<span data-ttu-id="4e4bd-117">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="4e4bd-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e4bd-118">-Confirm</span></span>
<span data-ttu-id="4e4bd-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e4bd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e4bd-120">-WhatIf</span></span>
<span data-ttu-id="4e4bd-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e4bd-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e4bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4bd-123">CommonParameters</span></span>
<span data-ttu-id="4e4bd-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4bd-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e4bd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4bd-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e4bd-126">INPUTS</span></span>

## <span data-ttu-id="4e4bd-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e4bd-127">OUTPUTS</span></span>

## <span data-ttu-id="4e4bd-128">Note</span><span class="sxs-lookup"><span data-stu-id="4e4bd-128">NOTES</span></span>

## <span data-ttu-id="4e4bd-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e4bd-129">RELATED LINKS</span></span>

[<span data-ttu-id="4e4bd-130">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4e4bd-130">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="4e4bd-131">Registro-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4e4bd-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


