---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
ms.openlocfilehash: 2f0f4ea68de5071a860b55a464d339d65ff2882c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508255"
---
# <span data-ttu-id="879fa-101">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="879fa-101">Get-AzureRmDataFactory</span></span>

## <span data-ttu-id="879fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="879fa-102">SYNOPSIS</span></span>
<span data-ttu-id="879fa-103">Ottiene informazioni sulle Factory di dati.</span><span class="sxs-lookup"><span data-stu-id="879fa-103">Gets information about Data Factories.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="879fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="879fa-104">SYNTAX</span></span>

```
Get-AzureRmDataFactory [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="879fa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="879fa-105">DESCRIPTION</span></span>
<span data-ttu-id="879fa-106">Il cmdlet **Get-AzureRmDataFactory** ottiene informazioni sulle Factory di dati in un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="879fa-106">The **Get-AzureRmDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="879fa-107">Se specifichi il nome di una data factory, questo cmdlet ottiene informazioni su tale data factory.</span><span class="sxs-lookup"><span data-stu-id="879fa-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="879fa-108">Se non specifichi un nome, questo cmdlet recupera informazioni su tutti i factory di dati in un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="879fa-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="879fa-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="879fa-109">EXAMPLES</span></span>

### <span data-ttu-id="879fa-110">Esempio 1: ottenere tutte le factory di dati</span><span class="sxs-lookup"><span data-stu-id="879fa-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzureRmDataFactory -ResourceGroupName "ADF"
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

<span data-ttu-id="879fa-111">Questo comando Visualizza informazioni su tutti i factory di dati nell'abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="879fa-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="879fa-112">Esempio 2: ottenere una factory di dati specifica</span><span class="sxs-lookup"><span data-stu-id="879fa-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="879fa-113">Questo comando Visualizza le informazioni sulla factory di dati denominate WikiADF nell'abbonamento per il gruppo di risorse denominato ADF e lo archivia nella variabile $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="879fa-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="879fa-114">Specifica il parametro *DataFactory* nei cmdlet successivi per usare la factory di dati archiviata in $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="879fa-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="879fa-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="879fa-115">PARAMETERS</span></span>

### <span data-ttu-id="879fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="879fa-116">-DefaultProfile</span></span>
<span data-ttu-id="879fa-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="879fa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="879fa-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="879fa-118">-Name</span></span>
<span data-ttu-id="879fa-119">Specifica il nome della factory di dati per cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="879fa-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="879fa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="879fa-120">-ResourceGroupName</span></span>
<span data-ttu-id="879fa-121">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="879fa-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="879fa-122">Questo cmdlet ottiene informazioni sulle Factory di dati che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="879fa-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="879fa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="879fa-123">CommonParameters</span></span>
<span data-ttu-id="879fa-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="879fa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="879fa-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="879fa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="879fa-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="879fa-126">INPUTS</span></span>

### <span data-ttu-id="879fa-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="879fa-127">None</span></span>
<span data-ttu-id="879fa-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="879fa-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="879fa-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="879fa-129">OUTPUTS</span></span>

### <span data-ttu-id="879fa-130">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="879fa-130">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="879fa-131">Note</span><span class="sxs-lookup"><span data-stu-id="879fa-131">NOTES</span></span>
* <span data-ttu-id="879fa-132">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="879fa-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="879fa-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="879fa-133">RELATED LINKS</span></span>

[<span data-ttu-id="879fa-134">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="879fa-134">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)

[<span data-ttu-id="879fa-135">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="879fa-135">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)

