---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 11ff763dacc5a6969501dae925fbbc2382c871b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856365"
---
# <span data-ttu-id="9d5c8-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="9d5c8-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="9d5c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5c8-103">Registra un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="9d5c8-103">Registers a resource provider.</span></span>

## <span data-ttu-id="9d5c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d5c8-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d5c8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="9d5c8-106">Il cmdlet **Register-AzResourceProvider** registra un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="9d5c8-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="9d5c8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d5c8-107">EXAMPLES</span></span>

### <span data-ttu-id="9d5c8-108">Esempio 1: registrare un provider</span><span class="sxs-lookup"><span data-stu-id="9d5c8-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="9d5c8-109">Questo registra il provider Microsoft. Network per l'account.</span><span class="sxs-lookup"><span data-stu-id="9d5c8-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="9d5c8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d5c8-110">PARAMETERS</span></span>

### <span data-ttu-id="9d5c8-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9d5c8-111">-ApiVersion</span></span>
<span data-ttu-id="9d5c8-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="9d5c8-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="9d5c8-113">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9d5c8-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="9d5c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d5c8-114">-DefaultProfile</span></span>
<span data-ttu-id="9d5c8-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9d5c8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d5c8-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="9d5c8-116">-Pre</span></span>
<span data-ttu-id="9d5c8-117">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="9d5c8-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9d5c8-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="9d5c8-118">-ProviderNamespace</span></span>
<span data-ttu-id="9d5c8-119">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="9d5c8-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="9d5c8-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d5c8-120">-Confirm</span></span>
<span data-ttu-id="9d5c8-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d5c8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d5c8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d5c8-122">-WhatIf</span></span>
<span data-ttu-id="9d5c8-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d5c8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d5c8-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d5c8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d5c8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5c8-125">CommonParameters</span></span>
<span data-ttu-id="9d5c8-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d5c8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5c8-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d5c8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5c8-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d5c8-128">INPUTS</span></span>

### <span data-ttu-id="9d5c8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9d5c8-129">System.String</span></span>

## <span data-ttu-id="9d5c8-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d5c8-130">OUTPUTS</span></span>

### <span data-ttu-id="9d5c8-131">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="9d5c8-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="9d5c8-132">Note</span><span class="sxs-lookup"><span data-stu-id="9d5c8-132">NOTES</span></span>

## <span data-ttu-id="9d5c8-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d5c8-133">RELATED LINKS</span></span>

[<span data-ttu-id="9d5c8-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="9d5c8-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="9d5c8-135">Annullamento della registrazione-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="9d5c8-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


