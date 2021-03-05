---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: c13fdf46dff4ba0b62a8009bad7c4790507b2561
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975006"
---
# <span data-ttu-id="434f5-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="434f5-101">New-AzDataFactory</span></span>

## <span data-ttu-id="434f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="434f5-102">SYNOPSIS</span></span>
<span data-ttu-id="434f5-103">Crea un data factory.</span><span class="sxs-lookup"><span data-stu-id="434f5-103">Creates a data factory.</span></span>

## <span data-ttu-id="434f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="434f5-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="434f5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="434f5-105">DESCRIPTION</span></span>
<span data-ttu-id="434f5-106">Il cmdlet **New-AzDataFactory crea** una data factory con il nome e la posizione del gruppo di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="434f5-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="434f5-107">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="434f5-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="434f5-108">Creare un data factory.</span><span class="sxs-lookup"><span data-stu-id="434f5-108">Create a data factory.</span></span> 
- <span data-ttu-id="434f5-109">Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="434f5-109">Create linked services.</span></span> 
- <span data-ttu-id="434f5-110">Creare set di dati.</span><span class="sxs-lookup"><span data-stu-id="434f5-110">Create datasets.</span></span> 
- <span data-ttu-id="434f5-111">Creare una pipeline.</span><span class="sxs-lookup"><span data-stu-id="434f5-111">Create a pipeline.</span></span>

## <span data-ttu-id="434f5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="434f5-112">EXAMPLES</span></span>

### <span data-ttu-id="434f5-113">Esempio 1: Creare un data factory</span><span class="sxs-lookup"><span data-stu-id="434f5-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="434f5-114">Questo comando crea un data factory denominato WikiADF nel gruppo di risorse denominato ADF nella posizione WestUS.</span><span class="sxs-lookup"><span data-stu-id="434f5-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="434f5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="434f5-115">PARAMETERS</span></span>

### <span data-ttu-id="434f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434f5-116">-DefaultProfile</span></span>
<span data-ttu-id="434f5-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="434f5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="434f5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="434f5-118">-Force</span></span>
<span data-ttu-id="434f5-119">Indica che questo cmdlet sostituisce un data factory esistente senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="434f5-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="434f5-120">-Location</span><span class="sxs-lookup"><span data-stu-id="434f5-120">-Location</span></span>
<span data-ttu-id="434f5-121">Specifica la posizione del data factory, ad esempio WestUS o EastUS.</span><span class="sxs-lookup"><span data-stu-id="434f5-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="434f5-122">Attualmente è supportato solo WestUS.</span><span class="sxs-lookup"><span data-stu-id="434f5-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="434f5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="434f5-123">-Name</span></span>
<span data-ttu-id="434f5-124">Specifica il nome del data factory da creare.</span><span class="sxs-lookup"><span data-stu-id="434f5-124">Specifies the name of the data factory to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434f5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="434f5-125">-ResourceGroupName</span></span>
<span data-ttu-id="434f5-126">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="434f5-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="434f5-127">Questo cmdlet crea un data factory che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="434f5-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="434f5-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="434f5-128">-Tag</span></span>
<span data-ttu-id="434f5-129">I tag del data factory.</span><span class="sxs-lookup"><span data-stu-id="434f5-129">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434f5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="434f5-130">-Confirm</span></span>
<span data-ttu-id="434f5-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="434f5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="434f5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="434f5-132">-WhatIf</span></span>
<span data-ttu-id="434f5-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="434f5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="434f5-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="434f5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="434f5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434f5-135">CommonParameters</span></span>
<span data-ttu-id="434f5-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="434f5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434f5-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="434f5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434f5-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="434f5-138">INPUTS</span></span>

### <span data-ttu-id="434f5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="434f5-139">System.String</span></span>

### <span data-ttu-id="434f5-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="434f5-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="434f5-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="434f5-141">OUTPUTS</span></span>

### <span data-ttu-id="434f5-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="434f5-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="434f5-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="434f5-143">NOTES</span></span>
* <span data-ttu-id="434f5-144">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="434f5-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="434f5-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="434f5-145">RELATED LINKS</span></span>

[<span data-ttu-id="434f5-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="434f5-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="434f5-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="434f5-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


