---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: a7c30ee436f35bee72e786c1d219e114236248da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519536"
---
# <span data-ttu-id="27a5b-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="27a5b-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="27a5b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="27a5b-103">Ottiene un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="27a5b-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27a5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27a5b-104">SYNTAX</span></span>

### <span data-ttu-id="27a5b-105">ListAvailable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27a5b-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27a5b-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="27a5b-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27a5b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27a5b-107">DESCRIPTION</span></span>
<span data-ttu-id="27a5b-108">Il cmdlet **Get-AzureRmResourceProvider** ottiene un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="27a5b-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="27a5b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27a5b-109">EXAMPLES</span></span>

## <span data-ttu-id="27a5b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27a5b-110">PARAMETERS</span></span>

### <span data-ttu-id="27a5b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="27a5b-111">-ApiVersion</span></span>
<span data-ttu-id="27a5b-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="27a5b-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="27a5b-113">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="27a5b-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="27a5b-114">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="27a5b-114">-ListAvailable</span></span>
<span data-ttu-id="27a5b-115">Indica che questa operazione ottiene tutti i provider di risorse disponibili.</span><span class="sxs-lookup"><span data-stu-id="27a5b-115">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a5b-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="27a5b-116">-Location</span></span>
<span data-ttu-id="27a5b-117">Specifica la posizione del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="27a5b-117">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="27a5b-118">-Pre</span><span class="sxs-lookup"><span data-stu-id="27a5b-118">-Pre</span></span>
<span data-ttu-id="27a5b-119">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="27a5b-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="27a5b-120">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="27a5b-120">-ProviderNamespace</span></span>
<span data-ttu-id="27a5b-121">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="27a5b-121">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: IndividualProvider
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a5b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a5b-122">-DefaultProfile</span></span>
<span data-ttu-id="27a5b-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27a5b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27a5b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a5b-124">CommonParameters</span></span>
<span data-ttu-id="27a5b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27a5b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a5b-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27a5b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a5b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27a5b-127">INPUTS</span></span>

## <span data-ttu-id="27a5b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27a5b-128">OUTPUTS</span></span>

### <span data-ttu-id="27a5b-129">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="27a5b-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="27a5b-130">Note</span><span class="sxs-lookup"><span data-stu-id="27a5b-130">NOTES</span></span>

## <span data-ttu-id="27a5b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27a5b-131">RELATED LINKS</span></span>

[<span data-ttu-id="27a5b-132">Registro-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="27a5b-132">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="27a5b-133">Annullamento della registrazione-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="27a5b-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


