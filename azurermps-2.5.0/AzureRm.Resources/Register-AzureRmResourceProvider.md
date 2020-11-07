---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: c3459a07eb6f92e4ec30b5018efc41ff13e1c41e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866802"
---
# <span data-ttu-id="65c9d-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="65c9d-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="65c9d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="65c9d-103">Registra un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="65c9d-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65c9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65c9d-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65c9d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65c9d-105">DESCRIPTION</span></span>
<span data-ttu-id="65c9d-106">Il cmdlet **Register-AzureRmResourceProvider** registra un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="65c9d-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="65c9d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65c9d-107">EXAMPLES</span></span>

### <span data-ttu-id="65c9d-108">Esempio 1: registrare un provider</span><span class="sxs-lookup"><span data-stu-id="65c9d-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="65c9d-109">Questo registra il provider Microsoft. Network per l'account.</span><span class="sxs-lookup"><span data-stu-id="65c9d-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="65c9d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65c9d-110">PARAMETERS</span></span>

### <span data-ttu-id="65c9d-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="65c9d-111">-ApiVersion</span></span>
<span data-ttu-id="65c9d-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="65c9d-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="65c9d-113">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="65c9d-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="65c9d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c9d-114">-DefaultProfile</span></span>
<span data-ttu-id="65c9d-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="65c9d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65c9d-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="65c9d-116">-Pre</span></span>
<span data-ttu-id="65c9d-117">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="65c9d-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="65c9d-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="65c9d-118">-ProviderNamespace</span></span>
<span data-ttu-id="65c9d-119">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="65c9d-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="65c9d-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="65c9d-120">-Confirm</span></span>
<span data-ttu-id="65c9d-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65c9d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65c9d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65c9d-122">-WhatIf</span></span>
<span data-ttu-id="65c9d-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65c9d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65c9d-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65c9d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65c9d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c9d-125">CommonParameters</span></span>
<span data-ttu-id="65c9d-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65c9d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c9d-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65c9d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c9d-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65c9d-128">INPUTS</span></span>

## <span data-ttu-id="65c9d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65c9d-129">OUTPUTS</span></span>

## <span data-ttu-id="65c9d-130">Note</span><span class="sxs-lookup"><span data-stu-id="65c9d-130">NOTES</span></span>

## <span data-ttu-id="65c9d-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65c9d-131">RELATED LINKS</span></span>

[<span data-ttu-id="65c9d-132">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="65c9d-132">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="65c9d-133">Annullamento della registrazione-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="65c9d-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


