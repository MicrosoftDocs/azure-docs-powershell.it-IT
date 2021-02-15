---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: b84a5d6cbbf090243a63ad9919a3fbb1977d77f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207195"
---
# <span data-ttu-id="a08d3-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="a08d3-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="a08d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a08d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a08d3-103">Elimina un account di Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="a08d3-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="a08d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a08d3-104">SYNTAX</span></span>

### <span data-ttu-id="a08d3-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="a08d3-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a08d3-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a08d3-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a08d3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a08d3-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a08d3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a08d3-108">DESCRIPTION</span></span>
<span data-ttu-id="a08d3-109">Il Remove-AzMapsAccount cmdlet elimina l'account di Azure Maps specificato.</span><span class="sxs-lookup"><span data-stu-id="a08d3-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="a08d3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a08d3-110">EXAMPLES</span></span>

### <span data-ttu-id="a08d3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a08d3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="a08d3-112">Elimina l'account MyAccount dal gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a08d3-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="a08d3-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a08d3-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="a08d3-114">Elimina l'account di Azure Maps specificato.</span><span class="sxs-lookup"><span data-stu-id="a08d3-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="a08d3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a08d3-115">PARAMETERS</span></span>

### <span data-ttu-id="a08d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a08d3-116">-DefaultProfile</span></span>
<span data-ttu-id="a08d3-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a08d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a08d3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a08d3-118">-InputObject</span></span>
<span data-ttu-id="a08d3-119">Mappe dell'account in pipe da Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="a08d3-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="a08d3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a08d3-120">-Name</span></span>
<span data-ttu-id="a08d3-121">Nome account mappe.</span><span class="sxs-lookup"><span data-stu-id="a08d3-121">Maps Account Name.</span></span>

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

### <span data-ttu-id="a08d3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a08d3-122">-PassThru</span></span>
<span data-ttu-id="a08d3-123">Indica se l'account specificato è stato eliminato o meno.</span><span class="sxs-lookup"><span data-stu-id="a08d3-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="a08d3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a08d3-124">-ResourceGroupName</span></span>
<span data-ttu-id="a08d3-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a08d3-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a08d3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a08d3-126">-ResourceId</span></span>
<span data-ttu-id="a08d3-127">Mappe Id ResourceId account.</span><span class="sxs-lookup"><span data-stu-id="a08d3-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="a08d3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a08d3-128">-Confirm</span></span>
<span data-ttu-id="a08d3-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a08d3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a08d3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a08d3-130">-WhatIf</span></span>
<span data-ttu-id="a08d3-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a08d3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a08d3-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a08d3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a08d3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a08d3-133">CommonParameters</span></span>
<span data-ttu-id="a08d3-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a08d3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a08d3-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a08d3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a08d3-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="a08d3-136">INPUTS</span></span>

### <span data-ttu-id="a08d3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a08d3-137">System.String</span></span>

### <span data-ttu-id="a08d3-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="a08d3-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="a08d3-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a08d3-139">OUTPUTS</span></span>

### <span data-ttu-id="a08d3-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a08d3-140">System.Boolean</span></span>

## <span data-ttu-id="a08d3-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="a08d3-141">NOTES</span></span>

## <span data-ttu-id="a08d3-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a08d3-142">RELATED LINKS</span></span>
