---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: c179ac3657a69b908c605fbaf4d0577b8a77a90f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862313"
---
# <span data-ttu-id="b2202-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b2202-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="b2202-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2202-102">SYNOPSIS</span></span>
<span data-ttu-id="b2202-103">Annulla la registrazione di un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2202-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="b2202-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2202-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2202-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2202-105">DESCRIPTION</span></span>
<span data-ttu-id="b2202-106">Il cmdlet **Unregister-AzResourceProvider** Annulla la registrazione di un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="b2202-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="b2202-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2202-107">EXAMPLES</span></span>

## <span data-ttu-id="b2202-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2202-108">PARAMETERS</span></span>

### <span data-ttu-id="b2202-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b2202-109">-ApiVersion</span></span>
<span data-ttu-id="b2202-110">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2202-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b2202-111">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b2202-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b2202-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2202-112">-DefaultProfile</span></span>
<span data-ttu-id="b2202-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b2202-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2202-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="b2202-114">-Pre</span></span>
<span data-ttu-id="b2202-115">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b2202-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b2202-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="b2202-116">-ProviderNamespace</span></span>
<span data-ttu-id="b2202-117">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2202-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="b2202-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b2202-118">-Confirm</span></span>
<span data-ttu-id="b2202-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2202-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2202-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2202-120">-WhatIf</span></span>
<span data-ttu-id="b2202-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2202-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2202-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2202-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2202-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2202-123">CommonParameters</span></span>
<span data-ttu-id="b2202-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2202-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2202-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2202-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2202-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2202-126">INPUTS</span></span>

## <span data-ttu-id="b2202-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2202-127">OUTPUTS</span></span>

## <span data-ttu-id="b2202-128">Note</span><span class="sxs-lookup"><span data-stu-id="b2202-128">NOTES</span></span>

## <span data-ttu-id="b2202-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2202-129">RELATED LINKS</span></span>

[<span data-ttu-id="b2202-130">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b2202-130">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="b2202-131">Registro-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b2202-131">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


