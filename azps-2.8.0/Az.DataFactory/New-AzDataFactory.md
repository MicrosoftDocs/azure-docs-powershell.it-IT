---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: 0ad9af6702af457dbdc1a934c8c9e9dd29fb1162
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674992"
---
# <span data-ttu-id="1fc2f-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="1fc2f-101">New-AzDataFactory</span></span>

## <span data-ttu-id="1fc2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1fc2f-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc2f-103">Crea una data factory.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-103">Creates a data factory.</span></span>

## <span data-ttu-id="1fc2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1fc2f-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1fc2f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fc2f-105">DESCRIPTION</span></span>
<span data-ttu-id="1fc2f-106">Il cmdlet **New-AzDataFactory** crea una factory di dati con il nome e il percorso del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="1fc2f-107">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="1fc2f-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="1fc2f-108">Creare una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-108">Create a data factory.</span></span> 
- <span data-ttu-id="1fc2f-109">Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-109">Create linked services.</span></span> 
- <span data-ttu-id="1fc2f-110">Creare set di DataSet.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-110">Create datasets.</span></span> 
- <span data-ttu-id="1fc2f-111">Creare una pipeline.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-111">Create a pipeline.</span></span>

## <span data-ttu-id="1fc2f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1fc2f-112">EXAMPLES</span></span>

### <span data-ttu-id="1fc2f-113">Esempio 1: creare una data factory</span><span class="sxs-lookup"><span data-stu-id="1fc2f-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="1fc2f-114">Questo comando crea una factory di dati denominata WikiADF nel gruppo di risorse denominato ADF nella posizione Westus.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="1fc2f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1fc2f-115">PARAMETERS</span></span>

### <span data-ttu-id="1fc2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc2f-116">-DefaultProfile</span></span>
<span data-ttu-id="1fc2f-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1fc2f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fc2f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1fc2f-118">-Force</span></span>
<span data-ttu-id="1fc2f-119">Indica che questo cmdlet sostituisce una data factory esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1fc2f-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1fc2f-120">-Location</span></span>
<span data-ttu-id="1fc2f-121">Specifica la posizione per la data factory, ad esempio Westus o Eastus.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="1fc2f-122">Solo Westus è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="1fc2f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fc2f-123">-Name</span></span>
<span data-ttu-id="1fc2f-124">Specifica il nome della factory di dati da creare.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="1fc2f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fc2f-125">-ResourceGroupName</span></span>
<span data-ttu-id="1fc2f-126">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1fc2f-127">Questo cmdlet crea una factory di dati che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1fc2f-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="1fc2f-128">-Tag</span></span>
<span data-ttu-id="1fc2f-129">Tag della data factory.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="1fc2f-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1fc2f-130">-Confirm</span></span>
<span data-ttu-id="1fc2f-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fc2f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fc2f-132">-WhatIf</span></span>
<span data-ttu-id="1fc2f-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fc2f-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fc2f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc2f-135">CommonParameters</span></span>
<span data-ttu-id="1fc2f-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fc2f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc2f-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fc2f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc2f-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1fc2f-138">INPUTS</span></span>

### <span data-ttu-id="1fc2f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1fc2f-139">System.String</span></span>

### <span data-ttu-id="1fc2f-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1fc2f-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1fc2f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1fc2f-141">OUTPUTS</span></span>

### <span data-ttu-id="1fc2f-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1fc2f-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="1fc2f-143">Note</span><span class="sxs-lookup"><span data-stu-id="1fc2f-143">NOTES</span></span>
* <span data-ttu-id="1fc2f-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="1fc2f-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1fc2f-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1fc2f-145">RELATED LINKS</span></span>

[<span data-ttu-id="1fc2f-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="1fc2f-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="1fc2f-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="1fc2f-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)

