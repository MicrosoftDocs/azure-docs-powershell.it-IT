---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: c6c689ce2c9ccda71150f221bdea4ae5dd2a20fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210083"
---
# <span data-ttu-id="f8c32-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="f8c32-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="f8c32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8c32-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c32-103">Ottenere o elencare le definizioni delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="f8c32-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="f8c32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8c32-104">SYNTAX</span></span>

### <span data-ttu-id="f8c32-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="f8c32-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8c32-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f8c32-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8c32-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f8c32-107">DESCRIPTION</span></span>
<span data-ttu-id="f8c32-108">Ottenere o elencare le definizioni delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="f8c32-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="f8c32-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8c32-109">EXAMPLES</span></span>

### <span data-ttu-id="f8c32-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f8c32-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="f8c32-111">Ottenere la definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="f8c32-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="f8c32-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f8c32-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image*

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="f8c32-113">Ottenere la definizione dell'immagine della raccolta che inizia con "immagine".</span><span class="sxs-lookup"><span data-stu-id="f8c32-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="f8c32-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f8c32-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="f8c32-115">Ottenere le definizioni delle immagini della raccolta in raccolta1.</span><span class="sxs-lookup"><span data-stu-id="f8c32-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="f8c32-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8c32-116">PARAMETERS</span></span>

### <span data-ttu-id="f8c32-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c32-117">-DefaultProfile</span></span>
<span data-ttu-id="f8c32-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c32-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8c32-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="f8c32-119">-GalleryName</span></span>
<span data-ttu-id="f8c32-120">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="f8c32-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="f8c32-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f8c32-121">-Name</span></span>
<span data-ttu-id="f8c32-122">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="f8c32-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f8c32-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8c32-123">-ResourceGroupName</span></span>
<span data-ttu-id="f8c32-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f8c32-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="f8c32-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8c32-125">-ResourceId</span></span>
<span data-ttu-id="f8c32-126">ID risorsa per la definizione dell'immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="f8c32-126">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="f8c32-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c32-127">CommonParameters</span></span>
<span data-ttu-id="f8c32-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8c32-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c32-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f8c32-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c32-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="f8c32-130">INPUTS</span></span>

### <span data-ttu-id="f8c32-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f8c32-131">System.String</span></span>

## <span data-ttu-id="f8c32-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8c32-132">OUTPUTS</span></span>

### <span data-ttu-id="f8c32-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="f8c32-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="f8c32-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="f8c32-134">NOTES</span></span>

## <span data-ttu-id="f8c32-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8c32-135">RELATED LINKS</span></span>
