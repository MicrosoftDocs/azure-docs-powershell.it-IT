---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 91e1bb556f2464f535e64a870b5491fceb9eac4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971262"
---
# <span data-ttu-id="e57e6-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="e57e6-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="e57e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e57e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e57e6-103">Crea un hub per un Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="e57e6-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="e57e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e57e6-104">SYNTAX</span></span>

### <span data-ttu-id="e57e6-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="e57e6-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e57e6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e57e6-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e57e6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e57e6-107">DESCRIPTION</span></span>
<span data-ttu-id="e57e6-108">Il cmdlet **New-AzDataHubHub** crea un hub per Data factory di Azure nel gruppo di risorse Azure specificato e nella data factory specificata con la definizione di file specificata.</span><span class="sxs-lookup"><span data-stu-id="e57e6-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="e57e6-109">Dopo aver creato l'hub, è possibile usarlo per archiviare e gestire i servizi collegati in un gruppo e aggiungere pipeline all'hub.</span><span class="sxs-lookup"><span data-stu-id="e57e6-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="e57e6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e57e6-110">EXAMPLES</span></span>

### <span data-ttu-id="e57e6-111">Esempio 1: Creare un hub</span><span class="sxs-lookup"><span data-stu-id="e57e6-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="e57e6-112">Questo comando crea un hub denominato ContosoDataHub nel gruppo di risorse ADFResourceGroup e il data factory denominato ADFDataWith.</span><span class="sxs-lookup"><span data-stu-id="e57e6-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="e57e6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e57e6-113">PARAMETERS</span></span>

### <span data-ttu-id="e57e6-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e57e6-114">-DataFactory</span></span>
<span data-ttu-id="e57e6-115">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="e57e6-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e57e6-116">Questo cmdlet crea un hub per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e57e6-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e57e6-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e57e6-117">-DataFactoryName</span></span>
<span data-ttu-id="e57e6-118">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="e57e6-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e57e6-119">Questo cmdlet crea un hub per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e57e6-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e57e6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e57e6-120">-DefaultProfile</span></span>
<span data-ttu-id="e57e6-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e57e6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e57e6-122">-File</span><span class="sxs-lookup"><span data-stu-id="e57e6-122">-File</span></span>
<span data-ttu-id="e57e6-123">Specifica il percorso completo del file JSON (JavaScript Object Notation) che contiene la descrizione dell'hub.</span><span class="sxs-lookup"><span data-stu-id="e57e6-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57e6-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e57e6-124">-Force</span></span>
<span data-ttu-id="e57e6-125">Indica che questo cmdlet sostituisce un hub esistente senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e57e6-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e57e6-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e57e6-126">-Name</span></span>
<span data-ttu-id="e57e6-127">Specifica il nome dell'hub da creare.</span><span class="sxs-lookup"><span data-stu-id="e57e6-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="e57e6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e57e6-128">-ResourceGroupName</span></span>
<span data-ttu-id="e57e6-129">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="e57e6-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e57e6-130">Questo cmdlet crea un hub che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e57e6-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e57e6-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e57e6-131">-Confirm</span></span>
<span data-ttu-id="e57e6-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e57e6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e57e6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e57e6-133">-WhatIf</span></span>
<span data-ttu-id="e57e6-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e57e6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e57e6-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e57e6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e57e6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57e6-136">CommonParameters</span></span>
<span data-ttu-id="e57e6-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e57e6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57e6-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e57e6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57e6-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="e57e6-139">INPUTS</span></span>

### <span data-ttu-id="e57e6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e57e6-140">System.String</span></span>

### <span data-ttu-id="e57e6-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e57e6-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="e57e6-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e57e6-142">OUTPUTS</span></span>

### <span data-ttu-id="e57e6-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="e57e6-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="e57e6-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="e57e6-144">NOTES</span></span>
* <span data-ttu-id="e57e6-145">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="e57e6-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e57e6-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e57e6-146">RELATED LINKS</span></span>

[<span data-ttu-id="e57e6-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="e57e6-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="e57e6-148">Remove-AzDataHub</span><span class="sxs-lookup"><span data-stu-id="e57e6-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


