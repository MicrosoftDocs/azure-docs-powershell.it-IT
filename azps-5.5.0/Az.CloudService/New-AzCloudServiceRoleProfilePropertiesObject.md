---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceRoleProfilePropertiesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
ms.openlocfilehash: c9e41a6a4fa7a89db31304dc343da466e8632a74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181790"
---
# <span data-ttu-id="bd330-101">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="bd330-101">New-AzCloudServiceRoleProfilePropertiesObject</span></span>

## <span data-ttu-id="bd330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd330-102">SYNOPSIS</span></span>
<span data-ttu-id="bd330-103">Creare un oggetto in memoria per CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="bd330-103">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="bd330-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd330-104">SYNTAX</span></span>

```
New-AzCloudServiceRoleProfilePropertiesObject [-Name <String>] [-SkuCapacity <Int64>] [-SkuName <String>]
 [-SkuTier <String>] [<CommonParameters>]
```

## <span data-ttu-id="bd330-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bd330-105">DESCRIPTION</span></span>
<span data-ttu-id="bd330-106">Creare un oggetto in memoria per CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="bd330-106">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="bd330-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd330-107">EXAMPLES</span></span>

### <span data-ttu-id="bd330-108">Esempio 1: Creare l'oggetto proprietà del profilo ruolo</span><span class="sxs-lookup"><span data-stu-id="bd330-108">Example 1: Create role profile properties object</span></span>
```powershell
$role = New-AzCloudServiceRoleProfilePropertiesObject -Name 'WebRole' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
```

<span data-ttu-id="bd330-109">Questo comando crea l'oggetto delle proprietà del profilo ruolo usato per creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="bd330-109">This command creates role profile properties object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="bd330-110">Per altre informazioni, vedere New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="bd330-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="bd330-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd330-111">PARAMETERS</span></span>

### <span data-ttu-id="bd330-112">-Name</span><span class="sxs-lookup"><span data-stu-id="bd330-112">-Name</span></span>
<span data-ttu-id="bd330-113">Nome del profilo del ruolo.</span><span class="sxs-lookup"><span data-stu-id="bd330-113">Name of role profile.</span></span>

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

### <span data-ttu-id="bd330-114">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="bd330-114">-SkuCapacity</span></span>
<span data-ttu-id="bd330-115">Specifica il numero di istanze di ruoli nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="bd330-115">Specifies the number of role instances in the cloud service.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd330-116">-SKUName</span><span class="sxs-lookup"><span data-stu-id="bd330-116">-SkuName</span></span>
<span data-ttu-id="bd330-117">Nome della SKU.</span><span class="sxs-lookup"><span data-stu-id="bd330-117">The sku name.</span></span>

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

### <span data-ttu-id="bd330-118">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="bd330-118">-SkuTier</span></span>
<span data-ttu-id="bd330-119">SkuTier.</span><span class="sxs-lookup"><span data-stu-id="bd330-119">SkuTier.</span></span>

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

### <span data-ttu-id="bd330-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd330-120">CommonParameters</span></span>
<span data-ttu-id="bd330-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd330-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd330-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bd330-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd330-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="bd330-123">INPUTS</span></span>

## <span data-ttu-id="bd330-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd330-124">OUTPUTS</span></span>

### <span data-ttu-id="bd330-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="bd330-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="bd330-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="bd330-126">NOTES</span></span>

<span data-ttu-id="bd330-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bd330-127">ALIASES</span></span>

## <span data-ttu-id="bd330-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd330-128">RELATED LINKS</span></span>

