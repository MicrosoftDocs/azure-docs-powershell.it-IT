---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: c115cd780750770e05bc55b1f70a7cfe33967fff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207210"
---
# <span data-ttu-id="e6bc6-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="e6bc6-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="e6bc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="e6bc6-103">Rigenera una chiave account.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-103">Regenerates an account key.</span></span>

## <span data-ttu-id="e6bc6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6bc6-104">SYNTAX</span></span>

### <span data-ttu-id="e6bc6-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="e6bc6-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6bc6-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6bc6-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6bc6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6bc6-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6bc6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e6bc6-108">DESCRIPTION</span></span>
<span data-ttu-id="e6bc6-109">Il cmdlet New-AzMapsAccountKey rigenera una chiave API per un account di Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="e6bc6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6bc6-110">EXAMPLES</span></span>

### <span data-ttu-id="e6bc6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e6bc6-111">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="e6bc6-112">Rigenera la chiave API primaria per l'account MyAccount nel gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="e6bc6-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e6bc6-113">Example 2</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="e6bc6-114">Rigenera la chiave API secondaria per l'account di Azure Maps specificato.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="e6bc6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6bc6-115">PARAMETERS</span></span>

### <span data-ttu-id="e6bc6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6bc6-116">-DefaultProfile</span></span>
<span data-ttu-id="e6bc6-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6bc6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6bc6-118">-InputObject</span></span>
<span data-ttu-id="e6bc6-119">Mappe dell'account in pipe da Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6bc6-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e6bc6-120">-KeyName</span></span>
<span data-ttu-id="e6bc6-121">Codice Account di Mappe.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-121">Maps Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6bc6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e6bc6-122">-Name</span></span>
<span data-ttu-id="e6bc6-123">Nome account mappe.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6bc6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6bc6-124">-ResourceGroupName</span></span>
<span data-ttu-id="e6bc6-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6bc6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6bc6-126">-ResourceId</span></span>
<span data-ttu-id="e6bc6-127">Mappe Id ResourceId account.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6bc6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6bc6-128">-Confirm</span></span>
<span data-ttu-id="e6bc6-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6bc6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6bc6-130">-WhatIf</span></span>
<span data-ttu-id="e6bc6-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6bc6-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6bc6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6bc6-133">CommonParameters</span></span>
<span data-ttu-id="e6bc6-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6bc6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6bc6-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6bc6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6bc6-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="e6bc6-136">INPUTS</span></span>

### <span data-ttu-id="e6bc6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e6bc6-137">System.String</span></span>

### <span data-ttu-id="e6bc6-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="e6bc6-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="e6bc6-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6bc6-139">OUTPUTS</span></span>

### <span data-ttu-id="e6bc6-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e6bc6-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="e6bc6-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="e6bc6-141">NOTES</span></span>

## <span data-ttu-id="e6bc6-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6bc6-142">RELATED LINKS</span></span>
