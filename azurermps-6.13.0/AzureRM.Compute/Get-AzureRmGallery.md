---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
ms.openlocfilehash: cdb703144daa6f9abd62aee41eaad94b2cfa50e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511891"
---
# <span data-ttu-id="c3c69-101">Get-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="c3c69-101">Get-AzureRmGallery</span></span>

## <span data-ttu-id="c3c69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3c69-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c69-103">Ottenere o elencare le raccolte.</span><span class="sxs-lookup"><span data-stu-id="c3c69-103">Get or list galleries.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3c69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3c69-104">SYNTAX</span></span>

### <span data-ttu-id="c3c69-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c3c69-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGallery [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3c69-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c3c69-106">ResourceIdParameter</span></span>
```
Get-AzureRmGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3c69-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3c69-107">DESCRIPTION</span></span>
<span data-ttu-id="c3c69-108">Ottenere o elencare le raccolte.</span><span class="sxs-lookup"><span data-stu-id="c3c69-108">Get or list galleries.</span></span>

## <span data-ttu-id="c3c69-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3c69-109">EXAMPLES</span></span>

### <span data-ttu-id="c3c69-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c3c69-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="c3c69-111">Ottenere la raccolta.</span><span class="sxs-lookup"><span data-stu-id="c3c69-111">Get the gallery.</span></span>

## <span data-ttu-id="c3c69-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3c69-112">PARAMETERS</span></span>

### <span data-ttu-id="c3c69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c69-113">-DefaultProfile</span></span>
<span data-ttu-id="c3c69-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3c69-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3c69-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3c69-115">-Name</span></span>
<span data-ttu-id="c3c69-116">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c3c69-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3c69-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3c69-117">-ResourceGroupName</span></span>
<span data-ttu-id="c3c69-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c3c69-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3c69-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3c69-119">-ResourceId</span></span>
<span data-ttu-id="c3c69-120">ID risorsa per la raccolta</span><span class="sxs-lookup"><span data-stu-id="c3c69-120">The resource id for Gallery</span></span>

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

### <span data-ttu-id="c3c69-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c69-121">CommonParameters</span></span>
<span data-ttu-id="c3c69-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3c69-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c69-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3c69-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c69-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3c69-124">INPUTS</span></span>

### <span data-ttu-id="c3c69-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c3c69-125">System.String</span></span>

### <span data-ttu-id="c3c69-126">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="c3c69-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="c3c69-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3c69-127">OUTPUTS</span></span>

### <span data-ttu-id="c3c69-128">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="c3c69-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="c3c69-129">Note</span><span class="sxs-lookup"><span data-stu-id="c3c69-129">NOTES</span></span>

## <span data-ttu-id="c3c69-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3c69-130">RELATED LINKS</span></span>
