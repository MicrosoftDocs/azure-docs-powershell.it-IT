---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: 54ce1d9fa73b29318597f5a1442712aabf7f92b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507996"
---
# <span data-ttu-id="2c9f3-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="2c9f3-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="2c9f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c9f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9f3-103">Ottiene un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="2c9f3-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c9f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c9f3-104">SYNTAX</span></span>

### <span data-ttu-id="2c9f3-105">ListAvailable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2c9f3-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c9f3-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="2c9f3-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c9f3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c9f3-107">DESCRIPTION</span></span>
<span data-ttu-id="2c9f3-108">Il cmdlet **Get-AzureRmResourceProvider** ottiene un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="2c9f3-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="2c9f3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c9f3-109">EXAMPLES</span></span>

## <span data-ttu-id="2c9f3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c9f3-110">PARAMETERS</span></span>

### <span data-ttu-id="2c9f3-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2c9f3-111">-ApiVersion</span></span>
<span data-ttu-id="2c9f3-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="2c9f3-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2c9f3-113">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2c9f3-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="2c9f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9f3-114">-DefaultProfile</span></span>
<span data-ttu-id="2c9f3-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2c9f3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c9f3-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="2c9f3-116">-ListAvailable</span></span>
<span data-ttu-id="2c9f3-117">Indica che questa operazione ottiene tutti i provider di risorse disponibili.</span><span class="sxs-lookup"><span data-stu-id="2c9f3-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9f3-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2c9f3-118">-Location</span></span>
<span data-ttu-id="2c9f3-119">Specifica la posizione del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="2c9f3-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="2c9f3-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="2c9f3-120">-Pre</span></span>
<span data-ttu-id="2c9f3-121">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="2c9f3-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2c9f3-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="2c9f3-122">-ProviderNamespace</span></span>
<span data-ttu-id="2c9f3-123">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="2c9f3-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: String
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9f3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9f3-124">CommonParameters</span></span>
<span data-ttu-id="2c9f3-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c9f3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9f3-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9f3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9f3-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c9f3-127">INPUTS</span></span>

### <span data-ttu-id="2c9f3-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2c9f3-128">None</span></span>
<span data-ttu-id="2c9f3-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2c9f3-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2c9f3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c9f3-130">OUTPUTS</span></span>

### <span data-ttu-id="2c9f3-131">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="2c9f3-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="2c9f3-132">Note</span><span class="sxs-lookup"><span data-stu-id="2c9f3-132">NOTES</span></span>

## <span data-ttu-id="2c9f3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c9f3-133">RELATED LINKS</span></span>

[<span data-ttu-id="2c9f3-134">Registro-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="2c9f3-134">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="2c9f3-135">Annullamento della registrazione-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="2c9f3-135">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


