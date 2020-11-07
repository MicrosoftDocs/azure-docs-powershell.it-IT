---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
ms.openlocfilehash: 1891ab463b007b2e4a1502579f0d0e0a48779ca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518143"
---
# <span data-ttu-id="61f16-101">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="61f16-101">New-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="61f16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61f16-102">SYNOPSIS</span></span>
<span data-ttu-id="61f16-103">Crea un hub per una factory di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="61f16-103">Creates a hub for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61f16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61f16-104">SYNTAX</span></span>

### <span data-ttu-id="61f16-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61f16-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61f16-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="61f16-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61f16-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61f16-107">DESCRIPTION</span></span>
<span data-ttu-id="61f16-108">Il cmdlet **New-AzureRmDataFactoryHub** crea un hub per Azure Data Factory nel gruppo di risorse Azure specificato e nella Factory di dati specificata con la definizione di file specificata.</span><span class="sxs-lookup"><span data-stu-id="61f16-108">The **New-AzureRmDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="61f16-109">Dopo aver creato l'hub, è possibile usarlo per archiviare e gestire i servizi collegati in un gruppo ed è possibile aggiungere pipeline all'hub.</span><span class="sxs-lookup"><span data-stu-id="61f16-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="61f16-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61f16-110">EXAMPLES</span></span>

### <span data-ttu-id="61f16-111">Esempio 1: creare un hub</span><span class="sxs-lookup"><span data-stu-id="61f16-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="61f16-112">Questo comando crea un Hub denominato ContosoDataHub nel gruppo di risorse ADFResourceGroup e la data factory denominata ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="61f16-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="61f16-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61f16-113">PARAMETERS</span></span>

### <span data-ttu-id="61f16-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="61f16-114">-DataFactory</span></span>
<span data-ttu-id="61f16-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="61f16-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="61f16-116">Questo cmdlet crea un hub per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="61f16-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f16-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="61f16-117">-DataFactoryName</span></span>
<span data-ttu-id="61f16-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="61f16-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="61f16-119">Questo cmdlet crea un hub per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="61f16-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f16-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f16-120">-DefaultProfile</span></span>
<span data-ttu-id="61f16-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="61f16-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f16-122">-File</span><span class="sxs-lookup"><span data-stu-id="61f16-122">-File</span></span>
<span data-ttu-id="61f16-123">Specifica il percorso completo del file JSON (JavaScript Object Notation) che contiene la descrizione dell'hub.</span><span class="sxs-lookup"><span data-stu-id="61f16-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f16-124">-Force</span><span class="sxs-lookup"><span data-stu-id="61f16-124">-Force</span></span>
<span data-ttu-id="61f16-125">Indica che questo cmdlet sostituisce un hub esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="61f16-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f16-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="61f16-126">-Name</span></span>
<span data-ttu-id="61f16-127">Specifica il nome dell'hub da creare.</span><span class="sxs-lookup"><span data-stu-id="61f16-127">Specifies the name of the hub to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f16-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f16-128">-ResourceGroupName</span></span>
<span data-ttu-id="61f16-129">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="61f16-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="61f16-130">Questo cmdlet crea un hub che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="61f16-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f16-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61f16-131">-Confirm</span></span>
<span data-ttu-id="61f16-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61f16-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f16-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f16-133">-WhatIf</span></span>
<span data-ttu-id="61f16-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61f16-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61f16-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61f16-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f16-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f16-136">CommonParameters</span></span>
<span data-ttu-id="61f16-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61f16-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f16-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f16-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f16-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61f16-139">INPUTS</span></span>

### <span data-ttu-id="61f16-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="61f16-140">None</span></span>
<span data-ttu-id="61f16-141">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="61f16-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61f16-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61f16-142">OUTPUTS</span></span>

### <span data-ttu-id="61f16-143">Microsoft. Azure. Commands. datafactories. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="61f16-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="61f16-144">Note</span><span class="sxs-lookup"><span data-stu-id="61f16-144">NOTES</span></span>
* <span data-ttu-id="61f16-145">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="61f16-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="61f16-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61f16-146">RELATED LINKS</span></span>

[<span data-ttu-id="61f16-147">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="61f16-147">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="61f16-148">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="61f16-148">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)

