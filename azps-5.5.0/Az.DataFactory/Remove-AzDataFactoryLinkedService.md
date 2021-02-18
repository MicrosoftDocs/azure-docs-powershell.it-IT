---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a8731b075ff5df71aa368fa0c1a3c94ade9ef9e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181006"
---
# <span data-ttu-id="1c3b7-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="1c3b7-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="1c3b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c3b7-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3b7-103">Rimuove un servizio collegato da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="1c3b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c3b7-104">SYNTAX</span></span>

### <span data-ttu-id="1c3b7-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="1c3b7-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c3b7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1c3b7-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c3b7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1c3b7-107">DESCRIPTION</span></span>
<span data-ttu-id="1c3b7-108">Il cmdlet **Remove-AzDataFactoryLinkedService** rimuove un servizio collegato da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="1c3b7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c3b7-109">EXAMPLES</span></span>

### <span data-ttu-id="1c3b7-110">Esempio 1: Rimuovere un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="1c3b7-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="1c3b7-111">Questo comando rimuove il servizio collegato denominato LinkedServiceTest dal data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="1c3b7-112">Questo comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="1c3b7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c3b7-113">PARAMETERS</span></span>

### <span data-ttu-id="1c3b7-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1c3b7-114">-DataFactory</span></span>
<span data-ttu-id="1c3b7-115">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="1c3b7-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1c3b7-116">Questo cmdlet rimuove un servizio collegato dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c3b7-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1c3b7-117">-DataFactoryName</span></span>
<span data-ttu-id="1c3b7-118">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1c3b7-119">Questo cmdlet rimuove un servizio collegato dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c3b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3b7-120">-DefaultProfile</span></span>
<span data-ttu-id="1c3b7-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="1c3b7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c3b7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1c3b7-122">-Force</span></span>
<span data-ttu-id="1c3b7-123">Indica che questo cmdlet rimuove un servizio collegato senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1c3b7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1c3b7-124">-Name</span></span>
<span data-ttu-id="1c3b7-125">Specifica il nome del servizio collegato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-125">Specifies the name of the linked service to remove.</span></span>

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

### <span data-ttu-id="1c3b7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c3b7-126">-ResourceGroupName</span></span>
<span data-ttu-id="1c3b7-127">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1c3b7-128">Questo cmdlet rimuove un servizio collegato dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c3b7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c3b7-129">-Confirm</span></span>
<span data-ttu-id="1c3b7-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c3b7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c3b7-131">-WhatIf</span></span>
<span data-ttu-id="1c3b7-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c3b7-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c3b7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3b7-134">CommonParameters</span></span>
<span data-ttu-id="1c3b7-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c3b7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3b7-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c3b7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3b7-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="1c3b7-137">INPUTS</span></span>

### <span data-ttu-id="1c3b7-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1c3b7-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="1c3b7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1c3b7-139">System.String</span></span>

## <span data-ttu-id="1c3b7-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c3b7-140">OUTPUTS</span></span>

### <span data-ttu-id="1c3b7-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="1c3b7-141">System.Void</span></span>

## <span data-ttu-id="1c3b7-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="1c3b7-142">NOTES</span></span>
* <span data-ttu-id="1c3b7-143">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="1c3b7-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1c3b7-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c3b7-144">RELATED LINKS</span></span>

[<span data-ttu-id="1c3b7-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="1c3b7-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="1c3b7-146">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="1c3b7-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


