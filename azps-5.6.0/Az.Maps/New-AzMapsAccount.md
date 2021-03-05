---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: b6a2e27f18a0ae9b7c98239d5acd1073922e149e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006669"
---
# <span data-ttu-id="e18e8-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="e18e8-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="e18e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e18e8-102">SYNOPSIS</span></span>
<span data-ttu-id="e18e8-103">Crea un account di Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="e18e8-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="e18e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e18e8-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e18e8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e18e8-105">DESCRIPTION</span></span>
<span data-ttu-id="e18e8-106">Il cmdlet New-AzMapsAccount crea un account di Azure Maps con la SKU specificata.</span><span class="sxs-lookup"><span data-stu-id="e18e8-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="e18e8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e18e8-107">EXAMPLES</span></span>

### <span data-ttu-id="e18e8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e18e8-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="e18e8-109">Crea un nuovo account di Azure Maps denominato MyAccount nel gruppo di risorse MyResourceGroup con lo SKU S0 e un tag.</span><span class="sxs-lookup"><span data-stu-id="e18e8-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="e18e8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e18e8-110">PARAMETERS</span></span>

### <span data-ttu-id="e18e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e18e8-111">-DefaultProfile</span></span>
<span data-ttu-id="e18e8-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e18e8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e18e8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e18e8-113">-Force</span></span>
<span data-ttu-id="e18e8-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e18e8-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e18e8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e18e8-115">-Name</span></span>
<span data-ttu-id="e18e8-116">Nome account mappe.</span><span class="sxs-lookup"><span data-stu-id="e18e8-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18e8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e18e8-117">-ResourceGroupName</span></span>
<span data-ttu-id="e18e8-118">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e18e8-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18e8-119">-SKUName</span><span class="sxs-lookup"><span data-stu-id="e18e8-119">-SkuName</span></span>
<span data-ttu-id="e18e8-120">Mappe nome SKU account.</span><span class="sxs-lookup"><span data-stu-id="e18e8-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18e8-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="e18e8-121">-Tag</span></span>
<span data-ttu-id="e18e8-122">Contrassegni account mappe.</span><span class="sxs-lookup"><span data-stu-id="e18e8-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e18e8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e18e8-123">-Confirm</span></span>
<span data-ttu-id="e18e8-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e18e8-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e18e8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e18e8-125">-WhatIf</span></span>
<span data-ttu-id="e18e8-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e18e8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e18e8-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e18e8-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e18e8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18e8-128">CommonParameters</span></span>
<span data-ttu-id="e18e8-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e18e8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18e8-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e18e8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18e8-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="e18e8-131">INPUTS</span></span>

### <span data-ttu-id="e18e8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e18e8-132">System.String</span></span>

## <span data-ttu-id="e18e8-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e18e8-133">OUTPUTS</span></span>

### <span data-ttu-id="e18e8-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="e18e8-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="e18e8-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="e18e8-135">NOTES</span></span>

## <span data-ttu-id="e18e8-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e18e8-136">RELATED LINKS</span></span>
