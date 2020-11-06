---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
ms.openlocfilehash: bff748b8c867b272208469d34229cc2724bc8610
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511875"
---
# <span data-ttu-id="d4e94-101">Get-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d4e94-101">Get-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="d4e94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4e94-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e94-103">Ottenere o elencare le versioni delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4e94-103">Get or list gallery image versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4e94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4e94-104">SYNTAX</span></span>

### <span data-ttu-id="d4e94-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4e94-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4e94-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d4e94-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4e94-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4e94-107">DESCRIPTION</span></span>
<span data-ttu-id="d4e94-108">Ottenere o elencare le versioni delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4e94-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="d4e94-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4e94-109">EXAMPLES</span></span>

### <span data-ttu-id="d4e94-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d4e94-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="d4e94-111">Ottenere la versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4e94-111">Get the gallery image version.</span></span>

## <span data-ttu-id="d4e94-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4e94-112">PARAMETERS</span></span>

### <span data-ttu-id="d4e94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e94-113">-DefaultProfile</span></span>
<span data-ttu-id="d4e94-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4e94-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4e94-115">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="d4e94-115">-ExpandReplicationStatus</span></span>
<span data-ttu-id="d4e94-116">Mostra lo stato di replica.</span><span class="sxs-lookup"><span data-stu-id="d4e94-116">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e94-117">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d4e94-117">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="d4e94-118">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4e94-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e94-119">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="d4e94-119">-GalleryName</span></span>
<span data-ttu-id="d4e94-120">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4e94-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e94-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4e94-121">-Name</span></span>
<span data-ttu-id="d4e94-122">Nome della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4e94-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e94-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e94-123">-ResourceGroupName</span></span>
<span data-ttu-id="d4e94-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4e94-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e94-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4e94-125">-ResourceId</span></span>
<span data-ttu-id="d4e94-126">ID risorsa per la versione dell'immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="d4e94-126">The resource ID for the gallery image version</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e94-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e94-127">CommonParameters</span></span>
<span data-ttu-id="d4e94-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4e94-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e94-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4e94-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e94-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4e94-130">INPUTS</span></span>

### <span data-ttu-id="d4e94-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d4e94-131">System.String</span></span>

### <span data-ttu-id="d4e94-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d4e94-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="d4e94-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4e94-133">OUTPUTS</span></span>

### <span data-ttu-id="d4e94-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d4e94-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="d4e94-135">Note</span><span class="sxs-lookup"><span data-stu-id="d4e94-135">NOTES</span></span>

## <span data-ttu-id="d4e94-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4e94-136">RELATED LINKS</span></span>
