---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 9e379df74f974e303faac300515e6bb7844e770b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686688"
---
# <span data-ttu-id="b91f2-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b91f2-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="b91f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b91f2-102">SYNOPSIS</span></span>
<span data-ttu-id="b91f2-103">Registra un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="b91f2-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b91f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b91f2-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b91f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b91f2-105">DESCRIPTION</span></span>
<span data-ttu-id="b91f2-106">Il cmdlet **Register-AzureRmResourceProvider** registra un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="b91f2-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="b91f2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b91f2-107">EXAMPLES</span></span>

### <span data-ttu-id="b91f2-108">Esempio 1: registrare un provider</span><span class="sxs-lookup"><span data-stu-id="b91f2-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="b91f2-109">Questo registra il provider Microsoft. Network per l'account.</span><span class="sxs-lookup"><span data-stu-id="b91f2-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="b91f2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b91f2-110">PARAMETERS</span></span>

### <span data-ttu-id="b91f2-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b91f2-111">-ApiVersion</span></span>
<span data-ttu-id="b91f2-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="b91f2-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b91f2-113">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b91f2-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b91f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b91f2-114">-DefaultProfile</span></span>
<span data-ttu-id="b91f2-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b91f2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b91f2-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="b91f2-116">-Pre</span></span>
<span data-ttu-id="b91f2-117">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b91f2-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b91f2-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="b91f2-118">-ProviderNamespace</span></span>
<span data-ttu-id="b91f2-119">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="b91f2-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="b91f2-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b91f2-120">-Confirm</span></span>
<span data-ttu-id="b91f2-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b91f2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b91f2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b91f2-122">-WhatIf</span></span>
<span data-ttu-id="b91f2-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b91f2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b91f2-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b91f2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b91f2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b91f2-125">CommonParameters</span></span>
<span data-ttu-id="b91f2-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b91f2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b91f2-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b91f2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b91f2-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b91f2-128">INPUTS</span></span>

### <span data-ttu-id="b91f2-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b91f2-129">None</span></span>
<span data-ttu-id="b91f2-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b91f2-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b91f2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b91f2-131">OUTPUTS</span></span>

### <span data-ttu-id="b91f2-132">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b91f2-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="b91f2-133">Note</span><span class="sxs-lookup"><span data-stu-id="b91f2-133">NOTES</span></span>

## <span data-ttu-id="b91f2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b91f2-134">RELATED LINKS</span></span>

[<span data-ttu-id="b91f2-135">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b91f2-135">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="b91f2-136">Annullamento della registrazione-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b91f2-136">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


