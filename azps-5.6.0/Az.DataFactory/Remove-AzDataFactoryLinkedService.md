---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: 28b2b5b1e2370e78c77178e3ee07056bacf1a896
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972045"
---
# <span data-ttu-id="cb6dc-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="cb6dc-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="cb6dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="cb6dc-103">Rimuove un servizio collegato da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="cb6dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb6dc-104">SYNTAX</span></span>

### <span data-ttu-id="cb6dc-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="cb6dc-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb6dc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cb6dc-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb6dc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cb6dc-107">DESCRIPTION</span></span>
<span data-ttu-id="cb6dc-108">Il cmdlet **Remove-AzDataFactoryLinkedService** rimuove un servizio collegato da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="cb6dc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb6dc-109">EXAMPLES</span></span>

### <span data-ttu-id="cb6dc-110">Esempio 1: Rimuovere un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="cb6dc-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="cb6dc-111">Questo comando rimuove il servizio collegato denominato LinkedServiceTest dal data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="cb6dc-112">Questo comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="cb6dc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb6dc-113">PARAMETERS</span></span>

### <span data-ttu-id="cb6dc-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb6dc-114">-DataFactory</span></span>
<span data-ttu-id="cb6dc-115">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="cb6dc-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cb6dc-116">Questo cmdlet rimuove un servizio collegato dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb6dc-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cb6dc-117">-DataFactoryName</span></span>
<span data-ttu-id="cb6dc-118">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cb6dc-119">Questo cmdlet rimuove un servizio collegato dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb6dc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb6dc-120">-DefaultProfile</span></span>
<span data-ttu-id="cb6dc-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cb6dc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb6dc-122">-Force</span><span class="sxs-lookup"><span data-stu-id="cb6dc-122">-Force</span></span>
<span data-ttu-id="cb6dc-123">Indica che questo cmdlet rimuove un servizio collegato senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="cb6dc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cb6dc-124">-Name</span></span>
<span data-ttu-id="cb6dc-125">Specifica il nome del servizio collegato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb6dc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb6dc-126">-ResourceGroupName</span></span>
<span data-ttu-id="cb6dc-127">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cb6dc-128">Questo cmdlet rimuove un servizio collegato dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb6dc-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb6dc-129">-Confirm</span></span>
<span data-ttu-id="cb6dc-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb6dc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb6dc-131">-WhatIf</span></span>
<span data-ttu-id="cb6dc-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb6dc-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb6dc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb6dc-134">CommonParameters</span></span>
<span data-ttu-id="cb6dc-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb6dc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb6dc-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb6dc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb6dc-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="cb6dc-137">INPUTS</span></span>

### <span data-ttu-id="cb6dc-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cb6dc-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="cb6dc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="cb6dc-139">System.String</span></span>

## <span data-ttu-id="cb6dc-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb6dc-140">OUTPUTS</span></span>

### <span data-ttu-id="cb6dc-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="cb6dc-141">System.Void</span></span>

## <span data-ttu-id="cb6dc-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="cb6dc-142">NOTES</span></span>
* <span data-ttu-id="cb6dc-143">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="cb6dc-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cb6dc-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb6dc-144">RELATED LINKS</span></span>

[<span data-ttu-id="cb6dc-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="cb6dc-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="cb6dc-146">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="cb6dc-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


