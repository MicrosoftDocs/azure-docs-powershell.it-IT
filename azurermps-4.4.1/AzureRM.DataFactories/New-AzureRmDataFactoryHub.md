---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
ms.openlocfilehash: d92cb12f051095a7e5de47d9c12b2c2329841bd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516244"
---
# <span data-ttu-id="eb86f-101">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="eb86f-101">New-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="eb86f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb86f-102">SYNOPSIS</span></span>
<span data-ttu-id="eb86f-103">Crea un hub per una factory di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="eb86f-103">Creates a hub for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb86f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb86f-104">SYNTAX</span></span>

### <span data-ttu-id="eb86f-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eb86f-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb86f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="eb86f-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb86f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb86f-107">DESCRIPTION</span></span>
<span data-ttu-id="eb86f-108">Il cmdlet **New-AzureRmDataFactoryHub** crea un hub per Azure Data Factory nel gruppo di risorse Azure specificato e nella Factory di dati specificata con la definizione di file specificata.</span><span class="sxs-lookup"><span data-stu-id="eb86f-108">The **New-AzureRmDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="eb86f-109">Dopo aver creato l'hub, è possibile usarlo per archiviare e gestire i servizi collegati in un gruppo ed è possibile aggiungere pipeline all'hub.</span><span class="sxs-lookup"><span data-stu-id="eb86f-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="eb86f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb86f-110">EXAMPLES</span></span>

### <span data-ttu-id="eb86f-111">Esempio 1: creare un hub</span><span class="sxs-lookup"><span data-stu-id="eb86f-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="eb86f-112">Questo comando crea un Hub denominato ContosoDataHub nel gruppo di risorse ADFResourceGroup e la data factory denominata ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="eb86f-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="eb86f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb86f-113">PARAMETERS</span></span>

### <span data-ttu-id="eb86f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="eb86f-114">-DataFactory</span></span>
<span data-ttu-id="eb86f-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="eb86f-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="eb86f-116">Questo cmdlet crea un hub per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="eb86f-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb86f-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="eb86f-117">-DataFactoryName</span></span>
<span data-ttu-id="eb86f-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="eb86f-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="eb86f-119">Questo cmdlet crea un hub per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="eb86f-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb86f-120">-File</span><span class="sxs-lookup"><span data-stu-id="eb86f-120">-File</span></span>
<span data-ttu-id="eb86f-121">Specifica il percorso completo del file JSON (JavaScript Object Notation) che contiene la descrizione dell'hub.</span><span class="sxs-lookup"><span data-stu-id="eb86f-121">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

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

### <span data-ttu-id="eb86f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="eb86f-122">-Force</span></span>
<span data-ttu-id="eb86f-123">Indica che questo cmdlet sostituisce un hub esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="eb86f-123">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="eb86f-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb86f-124">-Name</span></span>
<span data-ttu-id="eb86f-125">Specifica il nome dell'hub da creare.</span><span class="sxs-lookup"><span data-stu-id="eb86f-125">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="eb86f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb86f-126">-ResourceGroupName</span></span>
<span data-ttu-id="eb86f-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="eb86f-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="eb86f-128">Questo cmdlet crea un hub che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="eb86f-128">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb86f-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eb86f-129">-Confirm</span></span>
<span data-ttu-id="eb86f-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb86f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb86f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb86f-131">-WhatIf</span></span>
<span data-ttu-id="eb86f-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb86f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb86f-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb86f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb86f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb86f-134">-DefaultProfile</span></span>
<span data-ttu-id="eb86f-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb86f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb86f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb86f-136">CommonParameters</span></span>
<span data-ttu-id="eb86f-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb86f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb86f-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb86f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb86f-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb86f-139">INPUTS</span></span>

## <span data-ttu-id="eb86f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb86f-140">OUTPUTS</span></span>

### <span data-ttu-id="eb86f-141">Microsoft. Azure. Commands. datafactories. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="eb86f-141">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="eb86f-142">Note</span><span class="sxs-lookup"><span data-stu-id="eb86f-142">NOTES</span></span>
* <span data-ttu-id="eb86f-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="eb86f-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="eb86f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb86f-144">RELATED LINKS</span></span>

[<span data-ttu-id="eb86f-145">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="eb86f-145">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="eb86f-146">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="eb86f-146">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


