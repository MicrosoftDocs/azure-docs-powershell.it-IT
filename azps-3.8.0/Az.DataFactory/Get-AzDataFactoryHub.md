---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022218"
---
# <span data-ttu-id="ed547-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="ed547-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="ed547-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed547-102">SYNOPSIS</span></span>
<span data-ttu-id="ed547-103">Ottiene informazioni sugli hub in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ed547-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="ed547-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed547-104">SYNTAX</span></span>

### <span data-ttu-id="ed547-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed547-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed547-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ed547-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed547-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed547-107">DESCRIPTION</span></span>
<span data-ttu-id="ed547-108">Il cmdlet **Get-AzDataFactoryHub** ottiene le informazioni sugli hub in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ed547-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="ed547-109">Se specifichi il nome di un hub, questo cmdlet ottiene le informazioni su tale hub.</span><span class="sxs-lookup"><span data-stu-id="ed547-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="ed547-110">Se non specifichi un nome, questo cmdlet recupera le informazioni su tutti gli hub in una data factory.</span><span class="sxs-lookup"><span data-stu-id="ed547-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="ed547-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed547-111">EXAMPLES</span></span>

### <span data-ttu-id="ed547-112">Esempio 1: ottenere tutti gli hub dati</span><span class="sxs-lookup"><span data-stu-id="ed547-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="ed547-113">Questo comando consente di ottenere tutti gli hub dati nel gruppo di risorse Azure denominato ADFResourceGroup e la factory di dati denominata ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="ed547-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="ed547-114">Esempio 2: ottenere un hub dati specifico</span><span class="sxs-lookup"><span data-stu-id="ed547-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="ed547-115">Questo comando consente di ottenere informazioni sull'Hub denominato MyDataHub nel gruppo di risorse di Azure denominato ADFResourceGroup e nella Factory di dati denominata ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="ed547-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="ed547-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed547-116">PARAMETERS</span></span>

### <span data-ttu-id="ed547-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed547-117">-DataFactory</span></span>
<span data-ttu-id="ed547-118">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="ed547-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ed547-119">Questo cmdlet consente di ottenere informazioni sugli hub nella Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ed547-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed547-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ed547-120">-DataFactoryName</span></span>
<span data-ttu-id="ed547-121">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="ed547-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ed547-122">Questo cmdlet consente di ottenere informazioni sugli hub nella Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ed547-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed547-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed547-123">-DefaultProfile</span></span>
<span data-ttu-id="ed547-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ed547-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed547-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed547-125">-Name</span></span>
<span data-ttu-id="ed547-126">Specifica il nome dell'hub per cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="ed547-126">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed547-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed547-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed547-128">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="ed547-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ed547-129">Questo cmdlet recupera le informazioni sugli hub che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ed547-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed547-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed547-130">CommonParameters</span></span>
<span data-ttu-id="ed547-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed547-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed547-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed547-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed547-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed547-133">INPUTS</span></span>

### <span data-ttu-id="ed547-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ed547-134">System.String</span></span>

### <span data-ttu-id="ed547-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ed547-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ed547-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed547-136">OUTPUTS</span></span>

### <span data-ttu-id="ed547-137">Microsoft. Azure. Commands. datafactories. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="ed547-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="ed547-138">Note</span><span class="sxs-lookup"><span data-stu-id="ed547-138">NOTES</span></span>
* <span data-ttu-id="ed547-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="ed547-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ed547-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed547-140">RELATED LINKS</span></span>

[<span data-ttu-id="ed547-141">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="ed547-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="ed547-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="ed547-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


