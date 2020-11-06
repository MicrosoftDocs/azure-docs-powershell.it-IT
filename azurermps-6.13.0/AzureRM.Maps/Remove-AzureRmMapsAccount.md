---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/remove-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
ms.openlocfilehash: 9880bf574aec57796d185742b2f33b79da8f7c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510947"
---
# <span data-ttu-id="c4e38-101">Remove-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c4e38-101">Remove-AzureRmMapsAccount</span></span>

## <span data-ttu-id="c4e38-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4e38-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e38-103">Elimina un account di Azure maps.</span><span class="sxs-lookup"><span data-stu-id="c4e38-103">Deletes an Azure Maps account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4e38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4e38-104">SYNTAX</span></span>

### <span data-ttu-id="c4e38-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4e38-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4e38-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4e38-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4e38-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4e38-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4e38-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4e38-108">DESCRIPTION</span></span>
<span data-ttu-id="c4e38-109">Il cmdlet Remove-AzureRmMapsAccount Elimina l'account di Azure Maps specificato.</span><span class="sxs-lookup"><span data-stu-id="c4e38-109">The Remove-AzureRmMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="c4e38-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4e38-110">EXAMPLES</span></span>

### <span data-ttu-id="c4e38-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c4e38-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="c4e38-112">Consente di eliminare l'account dal gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c4e38-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="c4e38-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c4e38-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="c4e38-114">Elimina l'account di Azure Maps specificato.</span><span class="sxs-lookup"><span data-stu-id="c4e38-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="c4e38-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4e38-115">PARAMETERS</span></span>

### <span data-ttu-id="c4e38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e38-116">-DefaultProfile</span></span>
<span data-ttu-id="c4e38-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4e38-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4e38-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4e38-118">-InputObject</span></span>
<span data-ttu-id="c4e38-119">L'account di Maps viene inviato tramite pipe da Get-AzureRmMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="c4e38-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

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

### <span data-ttu-id="c4e38-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4e38-120">-Name</span></span>
<span data-ttu-id="c4e38-121">Nome dell'account mappe.</span><span class="sxs-lookup"><span data-stu-id="c4e38-121">Maps Account Name.</span></span>

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

### <span data-ttu-id="c4e38-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4e38-122">-PassThru</span></span>
<span data-ttu-id="c4e38-123">Restituirà se l'account specificato è stato eliminato o meno.</span><span class="sxs-lookup"><span data-stu-id="c4e38-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="c4e38-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4e38-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4e38-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c4e38-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c4e38-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4e38-126">-ResourceId</span></span>
<span data-ttu-id="c4e38-127">Mappe dell'account ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c4e38-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="c4e38-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c4e38-128">-Confirm</span></span>
<span data-ttu-id="c4e38-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4e38-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4e38-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4e38-130">-WhatIf</span></span>
<span data-ttu-id="c4e38-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4e38-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4e38-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4e38-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4e38-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e38-133">CommonParameters</span></span>
<span data-ttu-id="c4e38-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4e38-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e38-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4e38-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e38-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4e38-136">INPUTS</span></span>

### <span data-ttu-id="c4e38-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c4e38-137">System.String</span></span>

### <span data-ttu-id="c4e38-138">Microsoft. Azure. Commands. maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c4e38-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="c4e38-139">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c4e38-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c4e38-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4e38-140">OUTPUTS</span></span>

### <span data-ttu-id="c4e38-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4e38-141">System.Boolean</span></span>

## <span data-ttu-id="c4e38-142">Note</span><span class="sxs-lookup"><span data-stu-id="c4e38-142">NOTES</span></span>

## <span data-ttu-id="c4e38-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4e38-143">RELATED LINKS</span></span>
