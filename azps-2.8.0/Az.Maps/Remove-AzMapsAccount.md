---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: ba474ca3ea3a975262eec8b98df1fb99b0f336cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673872"
---
# <span data-ttu-id="73df7-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="73df7-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="73df7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73df7-102">SYNOPSIS</span></span>
<span data-ttu-id="73df7-103">Elimina un account di Azure maps.</span><span class="sxs-lookup"><span data-stu-id="73df7-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="73df7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73df7-104">SYNTAX</span></span>

### <span data-ttu-id="73df7-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73df7-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73df7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73df7-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73df7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73df7-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73df7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73df7-108">DESCRIPTION</span></span>
<span data-ttu-id="73df7-109">Il cmdlet Remove-AzMapsAccount Elimina l'account di Azure Maps specificato.</span><span class="sxs-lookup"><span data-stu-id="73df7-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="73df7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73df7-110">EXAMPLES</span></span>

### <span data-ttu-id="73df7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="73df7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="73df7-112">Consente di eliminare l'account dal gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="73df7-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="73df7-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="73df7-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="73df7-114">Elimina l'account di Azure Maps specificato.</span><span class="sxs-lookup"><span data-stu-id="73df7-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="73df7-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73df7-115">PARAMETERS</span></span>

### <span data-ttu-id="73df7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73df7-116">-DefaultProfile</span></span>
<span data-ttu-id="73df7-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73df7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73df7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73df7-118">-InputObject</span></span>
<span data-ttu-id="73df7-119">L'account di Maps viene inviato tramite pipe da Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="73df7-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="73df7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="73df7-120">-Name</span></span>
<span data-ttu-id="73df7-121">Nome dell'account mappe.</span><span class="sxs-lookup"><span data-stu-id="73df7-121">Maps Account Name.</span></span>

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

### <span data-ttu-id="73df7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73df7-122">-PassThru</span></span>
<span data-ttu-id="73df7-123">Restituirà se l'account specificato è stato eliminato o meno.</span><span class="sxs-lookup"><span data-stu-id="73df7-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="73df7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73df7-124">-ResourceGroupName</span></span>
<span data-ttu-id="73df7-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="73df7-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="73df7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73df7-126">-ResourceId</span></span>
<span data-ttu-id="73df7-127">Mappe dell'account ResourceId.</span><span class="sxs-lookup"><span data-stu-id="73df7-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="73df7-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="73df7-128">-Confirm</span></span>
<span data-ttu-id="73df7-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73df7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73df7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73df7-130">-WhatIf</span></span>
<span data-ttu-id="73df7-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73df7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73df7-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73df7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73df7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73df7-133">CommonParameters</span></span>
<span data-ttu-id="73df7-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73df7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73df7-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73df7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73df7-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73df7-136">INPUTS</span></span>

### <span data-ttu-id="73df7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="73df7-137">System.String</span></span>

### <span data-ttu-id="73df7-138">Microsoft. Azure. Commands. maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="73df7-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="73df7-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73df7-139">OUTPUTS</span></span>

### <span data-ttu-id="73df7-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73df7-140">System.Boolean</span></span>

## <span data-ttu-id="73df7-141">Note</span><span class="sxs-lookup"><span data-stu-id="73df7-141">NOTES</span></span>

## <span data-ttu-id="73df7-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73df7-142">RELATED LINKS</span></span>