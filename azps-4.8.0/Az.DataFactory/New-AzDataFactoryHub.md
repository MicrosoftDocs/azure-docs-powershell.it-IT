---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 1155b7c0b294ac3bc5c2106b473ce1cf55a9ac82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190278"
---
# <span data-ttu-id="78cf4-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="78cf4-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="78cf4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="78cf4-103">Crea un hub per una factory di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="78cf4-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="78cf4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78cf4-104">SYNTAX</span></span>

### <span data-ttu-id="78cf4-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78cf4-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78cf4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="78cf4-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78cf4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78cf4-107">DESCRIPTION</span></span>
<span data-ttu-id="78cf4-108">Il cmdlet **New-AzDataFactoryHub** crea un hub per Azure Data Factory nel gruppo di risorse Azure specificato e nella Factory di dati specificata con la definizione di file specificata.</span><span class="sxs-lookup"><span data-stu-id="78cf4-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="78cf4-109">Dopo aver creato l'hub, è possibile usarlo per archiviare e gestire i servizi collegati in un gruppo ed è possibile aggiungere pipeline all'hub.</span><span class="sxs-lookup"><span data-stu-id="78cf4-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="78cf4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78cf4-110">EXAMPLES</span></span>

### <span data-ttu-id="78cf4-111">Esempio 1: creare un hub</span><span class="sxs-lookup"><span data-stu-id="78cf4-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="78cf4-112">Questo comando crea un Hub denominato ContosoDataHub nel gruppo di risorse ADFResourceGroup e la data factory denominata ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="78cf4-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="78cf4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78cf4-113">PARAMETERS</span></span>

### <span data-ttu-id="78cf4-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="78cf4-114">-DataFactory</span></span>
<span data-ttu-id="78cf4-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="78cf4-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="78cf4-116">Questo cmdlet crea un hub per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="78cf4-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="78cf4-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="78cf4-117">-DataFactoryName</span></span>
<span data-ttu-id="78cf4-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="78cf4-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="78cf4-119">Questo cmdlet crea un hub per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="78cf4-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="78cf4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78cf4-120">-DefaultProfile</span></span>
<span data-ttu-id="78cf4-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="78cf4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78cf4-122">-File</span><span class="sxs-lookup"><span data-stu-id="78cf4-122">-File</span></span>
<span data-ttu-id="78cf4-123">Specifica il percorso completo del file JSON (JavaScript Object Notation) che contiene la descrizione dell'hub.</span><span class="sxs-lookup"><span data-stu-id="78cf4-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

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

### <span data-ttu-id="78cf4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="78cf4-124">-Force</span></span>
<span data-ttu-id="78cf4-125">Indica che questo cmdlet sostituisce un hub esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="78cf4-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="78cf4-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="78cf4-126">-Name</span></span>
<span data-ttu-id="78cf4-127">Specifica il nome dell'hub da creare.</span><span class="sxs-lookup"><span data-stu-id="78cf4-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="78cf4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78cf4-128">-ResourceGroupName</span></span>
<span data-ttu-id="78cf4-129">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="78cf4-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="78cf4-130">Questo cmdlet crea un hub che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="78cf4-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="78cf4-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="78cf4-131">-Confirm</span></span>
<span data-ttu-id="78cf4-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78cf4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78cf4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78cf4-133">-WhatIf</span></span>
<span data-ttu-id="78cf4-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78cf4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78cf4-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78cf4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78cf4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78cf4-136">CommonParameters</span></span>
<span data-ttu-id="78cf4-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78cf4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78cf4-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78cf4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78cf4-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78cf4-139">INPUTS</span></span>

### <span data-ttu-id="78cf4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="78cf4-140">System.String</span></span>

### <span data-ttu-id="78cf4-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="78cf4-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="78cf4-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78cf4-142">OUTPUTS</span></span>

### <span data-ttu-id="78cf4-143">Microsoft. Azure. Commands. datafactories. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="78cf4-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="78cf4-144">Note</span><span class="sxs-lookup"><span data-stu-id="78cf4-144">NOTES</span></span>
* <span data-ttu-id="78cf4-145">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="78cf4-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="78cf4-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78cf4-146">RELATED LINKS</span></span>

[<span data-ttu-id="78cf4-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="78cf4-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="78cf4-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="78cf4-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


