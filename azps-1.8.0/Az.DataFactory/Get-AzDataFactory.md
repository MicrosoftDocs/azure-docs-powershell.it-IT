---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 12028dfd15ca27f7d57f2ffa55e473c835e0391f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836563"
---
# <span data-ttu-id="b53d9-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="b53d9-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="b53d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b53d9-102">SYNOPSIS</span></span>
<span data-ttu-id="b53d9-103">Ottiene informazioni sulle Factory di dati.</span><span class="sxs-lookup"><span data-stu-id="b53d9-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="b53d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b53d9-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b53d9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b53d9-105">DESCRIPTION</span></span>
<span data-ttu-id="b53d9-106">Il cmdlet **Get-AzDataFactory** ottiene informazioni sulle Factory di dati in un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b53d9-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="b53d9-107">Se specifichi il nome di una data factory, questo cmdlet ottiene informazioni su tale data factory.</span><span class="sxs-lookup"><span data-stu-id="b53d9-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="b53d9-108">Se non specifichi un nome, questo cmdlet recupera informazioni su tutti i factory di dati in un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b53d9-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="b53d9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b53d9-109">EXAMPLES</span></span>

### <span data-ttu-id="b53d9-110">Esempio 1: ottenere tutte le factory di dati</span><span class="sxs-lookup"><span data-stu-id="b53d9-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzDataFactory -ResourceGroupName "ADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration

DataFactoryName   : WikiADF2
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="b53d9-111">Questo comando Visualizza informazioni su tutti i factory di dati nell'abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="b53d9-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="b53d9-112">Esempio 2: ottenere una factory di dati specifica</span><span class="sxs-lookup"><span data-stu-id="b53d9-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="b53d9-113">Questo comando Visualizza le informazioni sulla factory di dati denominate WikiADF nell'abbonamento per il gruppo di risorse denominato ADF e lo archivia nella variabile $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="b53d9-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="b53d9-114">Specifica il parametro *DataFactory* nei cmdlet successivi per usare la factory di dati archiviata in $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="b53d9-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="b53d9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b53d9-115">PARAMETERS</span></span>

### <span data-ttu-id="b53d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b53d9-116">-DefaultProfile</span></span>
<span data-ttu-id="b53d9-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b53d9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b53d9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b53d9-118">-Name</span></span>
<span data-ttu-id="b53d9-119">Specifica il nome della factory di dati per cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="b53d9-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b53d9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b53d9-120">-ResourceGroupName</span></span>
<span data-ttu-id="b53d9-121">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="b53d9-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b53d9-122">Questo cmdlet ottiene informazioni sulle Factory di dati che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b53d9-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b53d9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b53d9-123">CommonParameters</span></span>
<span data-ttu-id="b53d9-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b53d9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b53d9-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b53d9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b53d9-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b53d9-126">INPUTS</span></span>

### <span data-ttu-id="b53d9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b53d9-127">System.String</span></span>

## <span data-ttu-id="b53d9-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b53d9-128">OUTPUTS</span></span>

### <span data-ttu-id="b53d9-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b53d9-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="b53d9-130">Note</span><span class="sxs-lookup"><span data-stu-id="b53d9-130">NOTES</span></span>
* <span data-ttu-id="b53d9-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="b53d9-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b53d9-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b53d9-132">RELATED LINKS</span></span>

[<span data-ttu-id="b53d9-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="b53d9-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="b53d9-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="b53d9-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


