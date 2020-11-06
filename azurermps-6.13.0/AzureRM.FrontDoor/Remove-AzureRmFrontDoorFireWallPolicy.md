---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 4dda510402b9395db24507f22d90da0f1fb6a44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507439"
---
# <span data-ttu-id="e85ff-101">Remove-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="e85ff-101">Remove-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="e85ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e85ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e85ff-103">Rimuovere i criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="e85ff-103">Remove WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e85ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e85ff-104">SYNTAX</span></span>

### <span data-ttu-id="e85ff-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e85ff-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e85ff-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e85ff-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e85ff-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e85ff-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e85ff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e85ff-108">DESCRIPTION</span></span>
<span data-ttu-id="e85ff-109">Il cmdlet **Remove-AzureRmFrontDoor** rimuove un criterio WAF sotto la sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="e85ff-109">The **Remove-AzureRmFrontDoor** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="e85ff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e85ff-110">EXAMPLES</span></span>

### <span data-ttu-id="e85ff-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e85ff-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup
```

<span data-ttu-id="e85ff-112">Rimuovere i criteri di WAF denominati $name in $resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e85ff-112">Remove the WAF policy called $name in $resourceGroup.</span></span>

### <span data-ttu-id="e85ff-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e85ff-113">Example 2</span></span>
```powershell
PS C:\> Get--AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Remove-AzureRmFrontDoorFireWallPolicy
```

<span data-ttu-id="e85ff-114">Rimuovere tutti i criteri di WAF in $resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e85ff-114">Remove all WAF policy in $resourceGroup.</span></span>

## <span data-ttu-id="e85ff-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e85ff-115">PARAMETERS</span></span>

### <span data-ttu-id="e85ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e85ff-116">-DefaultProfile</span></span>
<span data-ttu-id="e85ff-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e85ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e85ff-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e85ff-118">-InputObject</span></span>
<span data-ttu-id="e85ff-119">Oggetto Criteri WAF da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e85ff-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e85ff-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e85ff-120">-Name</span></span>
<span data-ttu-id="e85ff-121">Il nome del criterio WAF da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e85ff-121">The name of the WAF policy to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e85ff-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e85ff-122">-PassThru</span></span>
<span data-ttu-id="e85ff-123">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="e85ff-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="e85ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e85ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="e85ff-125">Il gruppo di risorse a cui appartiene il criterio WAF.</span><span class="sxs-lookup"><span data-stu-id="e85ff-125">The resource group to which the WAF policy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e85ff-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e85ff-126">-ResourceId</span></span>
<span data-ttu-id="e85ff-127">ID risorsa dei criteri di WAF da eliminare</span><span class="sxs-lookup"><span data-stu-id="e85ff-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e85ff-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e85ff-128">-Confirm</span></span>
<span data-ttu-id="e85ff-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e85ff-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e85ff-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e85ff-130">-WhatIf</span></span>
<span data-ttu-id="e85ff-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e85ff-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e85ff-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e85ff-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e85ff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e85ff-133">CommonParameters</span></span>
<span data-ttu-id="e85ff-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e85ff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e85ff-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e85ff-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e85ff-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e85ff-136">INPUTS</span></span>

### <span data-ttu-id="e85ff-137">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="e85ff-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="e85ff-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e85ff-138">System.String</span></span>

### <span data-ttu-id="e85ff-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e85ff-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e85ff-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e85ff-140">OUTPUTS</span></span>

### <span data-ttu-id="e85ff-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e85ff-141">System.Boolean</span></span>

## <span data-ttu-id="e85ff-142">Note</span><span class="sxs-lookup"><span data-stu-id="e85ff-142">NOTES</span></span>

## <span data-ttu-id="e85ff-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e85ff-143">RELATED LINKS</span></span>

<span data-ttu-id="e85ff-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="e85ff-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span></span>
