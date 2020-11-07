---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 76a0164a5cf4c4d67ecb7f64667b9b87d9bc252c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854877"
---
# <span data-ttu-id="0fef1-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0fef1-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="0fef1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0fef1-102">SYNOPSIS</span></span>
<span data-ttu-id="0fef1-103">Ottiene un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="0fef1-103">Gets a resource provider.</span></span>

## <span data-ttu-id="0fef1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fef1-104">SYNTAX</span></span>

### <span data-ttu-id="0fef1-105">ListAvailable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0fef1-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fef1-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="0fef1-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fef1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fef1-107">DESCRIPTION</span></span>
<span data-ttu-id="0fef1-108">Il cmdlet **Get-AzResourceProvider** ottiene un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="0fef1-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="0fef1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fef1-109">EXAMPLES</span></span>

## <span data-ttu-id="0fef1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0fef1-110">PARAMETERS</span></span>

### <span data-ttu-id="0fef1-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0fef1-111">-ApiVersion</span></span>
<span data-ttu-id="0fef1-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="0fef1-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0fef1-113">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0fef1-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0fef1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fef1-114">-DefaultProfile</span></span>
<span data-ttu-id="0fef1-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0fef1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fef1-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="0fef1-116">-ListAvailable</span></span>
<span data-ttu-id="0fef1-117">Indica che questa operazione ottiene tutti i provider di risorse disponibili.</span><span class="sxs-lookup"><span data-stu-id="0fef1-117">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="0fef1-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0fef1-118">-Location</span></span>
<span data-ttu-id="0fef1-119">Specifica la posizione del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="0fef1-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="0fef1-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="0fef1-120">-Pre</span></span>
<span data-ttu-id="0fef1-121">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="0fef1-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0fef1-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="0fef1-122">-ProviderNamespace</span></span>
<span data-ttu-id="0fef1-123">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="0fef1-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fef1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fef1-124">CommonParameters</span></span>
<span data-ttu-id="0fef1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fef1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fef1-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fef1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fef1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0fef1-127">INPUTS</span></span>

### <span data-ttu-id="0fef1-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="0fef1-128">System.String[]</span></span>

## <span data-ttu-id="0fef1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fef1-129">OUTPUTS</span></span>

### <span data-ttu-id="0fef1-130">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0fef1-130">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="0fef1-131">Note</span><span class="sxs-lookup"><span data-stu-id="0fef1-131">NOTES</span></span>

## <span data-ttu-id="0fef1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fef1-132">RELATED LINKS</span></span>

[<span data-ttu-id="0fef1-133">Registro-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0fef1-133">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="0fef1-134">Annullamento della registrazione-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0fef1-134">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


