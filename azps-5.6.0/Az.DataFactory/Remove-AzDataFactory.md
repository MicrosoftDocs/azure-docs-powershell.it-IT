---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 3026f8774e08b3a5dd51b4ea905a5cb68dfd714a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957406"
---
# <span data-ttu-id="eff02-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="eff02-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="eff02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eff02-102">SYNOPSIS</span></span>
<span data-ttu-id="eff02-103">Rimuove un data factory.</span><span class="sxs-lookup"><span data-stu-id="eff02-103">Removes a data factory.</span></span>

## <span data-ttu-id="eff02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eff02-104">SYNTAX</span></span>

### <span data-ttu-id="eff02-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="eff02-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eff02-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="eff02-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eff02-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eff02-107">DESCRIPTION</span></span>
<span data-ttu-id="eff02-108">Il cmdlet **Remove-AzDataFactory** rimuove un data factory.</span><span class="sxs-lookup"><span data-stu-id="eff02-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="eff02-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eff02-109">EXAMPLES</span></span>

### <span data-ttu-id="eff02-110">Esempio 1: Rimuovere un data factory</span><span class="sxs-lookup"><span data-stu-id="eff02-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="eff02-111">Questo comando rimuove il data factory denominato WikiADF dal gruppo di risorse denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="eff02-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="eff02-112">Questo comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="eff02-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="eff02-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eff02-113">PARAMETERS</span></span>

### <span data-ttu-id="eff02-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="eff02-114">-DataFactory</span></span>
<span data-ttu-id="eff02-115">Specifica **l'oggetto PSDataFactory** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="eff02-115">Specifies the **PSDataFactory** object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eff02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff02-116">-DefaultProfile</span></span>
<span data-ttu-id="eff02-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="eff02-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eff02-118">-Force</span><span class="sxs-lookup"><span data-stu-id="eff02-118">-Force</span></span>
<span data-ttu-id="eff02-119">Indica che questo cmdlet rimuove un data factory senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="eff02-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="eff02-120">-Name</span><span class="sxs-lookup"><span data-stu-id="eff02-120">-Name</span></span>
<span data-ttu-id="eff02-121">Specifica il nome del data factory da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="eff02-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eff02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eff02-122">-ResourceGroupName</span></span>
<span data-ttu-id="eff02-123">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="eff02-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="eff02-124">Questo cmdlet rimuove un data factory dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="eff02-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eff02-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eff02-125">-Confirm</span></span>
<span data-ttu-id="eff02-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eff02-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eff02-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eff02-127">-WhatIf</span></span>
<span data-ttu-id="eff02-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eff02-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eff02-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eff02-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eff02-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff02-130">CommonParameters</span></span>
<span data-ttu-id="eff02-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eff02-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff02-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eff02-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff02-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="eff02-133">INPUTS</span></span>

### <span data-ttu-id="eff02-134">System.String</span><span class="sxs-lookup"><span data-stu-id="eff02-134">System.String</span></span>

### <span data-ttu-id="eff02-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="eff02-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="eff02-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eff02-136">OUTPUTS</span></span>

### <span data-ttu-id="eff02-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="eff02-137">System.Void</span></span>

## <span data-ttu-id="eff02-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="eff02-138">NOTES</span></span>
* <span data-ttu-id="eff02-139">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="eff02-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="eff02-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eff02-140">RELATED LINKS</span></span>

[<span data-ttu-id="eff02-141">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="eff02-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="eff02-142">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="eff02-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)


