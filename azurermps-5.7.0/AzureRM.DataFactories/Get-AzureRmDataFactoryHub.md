---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: cca0b397f85a0e0fd42f1e3331294881e1e89014
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685487"
---
# <span data-ttu-id="05e4e-101">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="05e4e-101">Get-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="05e4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="05e4e-103">Ottiene informazioni sugli hub in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="05e4e-103">Gets information about hubs in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05e4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05e4e-104">SYNTAX</span></span>

### <span data-ttu-id="05e4e-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="05e4e-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05e4e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="05e4e-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05e4e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05e4e-107">DESCRIPTION</span></span>
<span data-ttu-id="05e4e-108">Il cmdlet **Get-AzureRmDataFactoryHub** ottiene le informazioni sugli hub in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="05e4e-108">The **Get-AzureRmDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="05e4e-109">Se specifichi il nome di un hub, questo cmdlet ottiene le informazioni su tale hub.</span><span class="sxs-lookup"><span data-stu-id="05e4e-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="05e4e-110">Se non specifichi un nome, questo cmdlet recupera le informazioni su tutti gli hub in una data factory.</span><span class="sxs-lookup"><span data-stu-id="05e4e-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="05e4e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05e4e-111">EXAMPLES</span></span>

### <span data-ttu-id="05e4e-112">Esempio 1: ottenere tutti gli hub dati</span><span class="sxs-lookup"><span data-stu-id="05e4e-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="05e4e-113">Questo comando consente di ottenere tutti gli hub dati nel gruppo di risorse Azure denominato ADFResourceGroup e la factory di dati denominata ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="05e4e-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="05e4e-114">Esempio 2: ottenere un hub dati specifico</span><span class="sxs-lookup"><span data-stu-id="05e4e-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="05e4e-115">Questo comando consente di ottenere informazioni sull'Hub denominato MyDataHub nel gruppo di risorse di Azure denominato ADFResourceGroup e nella Factory di dati denominata ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="05e4e-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="05e4e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05e4e-116">PARAMETERS</span></span>

### <span data-ttu-id="05e4e-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="05e4e-117">-DataFactory</span></span>
<span data-ttu-id="05e4e-118">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="05e4e-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="05e4e-119">Questo cmdlet consente di ottenere informazioni sugli hub nella Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="05e4e-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="05e4e-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="05e4e-120">-DataFactoryName</span></span>
<span data-ttu-id="05e4e-121">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="05e4e-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="05e4e-122">Questo cmdlet consente di ottenere informazioni sugli hub nella Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="05e4e-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="05e4e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e4e-123">-DefaultProfile</span></span>
<span data-ttu-id="05e4e-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="05e4e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05e4e-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="05e4e-125">-Name</span></span>
<span data-ttu-id="05e4e-126">Specifica il nome dell'hub per cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="05e4e-126">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05e4e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05e4e-127">-ResourceGroupName</span></span>
<span data-ttu-id="05e4e-128">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="05e4e-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="05e4e-129">Questo cmdlet recupera le informazioni sugli hub che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="05e4e-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="05e4e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e4e-130">CommonParameters</span></span>
<span data-ttu-id="05e4e-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05e4e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e4e-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05e4e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e4e-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05e4e-133">INPUTS</span></span>

### <span data-ttu-id="05e4e-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="05e4e-134">None</span></span>
<span data-ttu-id="05e4e-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="05e4e-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05e4e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05e4e-136">OUTPUTS</span></span>

### <span data-ttu-id="05e4e-137">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. datafactories. Models. PSHub]</span><span class="sxs-lookup"><span data-stu-id="05e4e-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.DataFactories.Models.PSHub]</span></span>

### <span data-ttu-id="05e4e-138">Microsoft. Azure. Commands. datafactories. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="05e4e-138">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="05e4e-139">Note</span><span class="sxs-lookup"><span data-stu-id="05e4e-139">NOTES</span></span>
* <span data-ttu-id="05e4e-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="05e4e-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="05e4e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05e4e-141">RELATED LINKS</span></span>

[<span data-ttu-id="05e4e-142">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="05e4e-142">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)

[<span data-ttu-id="05e4e-143">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="05e4e-143">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


