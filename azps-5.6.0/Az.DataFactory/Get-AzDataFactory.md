---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: ff47851c998cb88bec7106e8aba6d47d16069321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977165"
---
# <span data-ttu-id="c1ba0-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="c1ba0-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="c1ba0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ba0-103">Ottiene informazioni su Data Factories.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="c1ba0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1ba0-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1ba0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c1ba0-105">DESCRIPTION</span></span>
<span data-ttu-id="c1ba0-106">Il cmdlet **Get-AzDataFactory ottiene** informazioni sulle fattorie di dati in un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="c1ba0-107">Se si specifica il nome di un data factory, questo cmdlet ottiene informazioni su tale data factory.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="c1ba0-108">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i data factories in un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="c1ba0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1ba0-109">EXAMPLES</span></span>

### <span data-ttu-id="c1ba0-110">Esempio 1: Ottenere tutti i data factories</span><span class="sxs-lookup"><span data-stu-id="c1ba0-110">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="c1ba0-111">Questo comando visualizza informazioni su tutti i data factories nella sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="c1ba0-112">Esempio 2: Ottenere un data factory specifico</span><span class="sxs-lookup"><span data-stu-id="c1ba0-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="c1ba0-113">Questo comando visualizza informazioni sul data factory denominato WikiADF nella sottoscrizione del gruppo di risorse denominato ADF e quindi lo archivia nella $DataFactory variabile.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="c1ba0-114">Specificare il *parametro DataFactory* nei cmdlet successivi per usare il data factory archiviato in $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="c1ba0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1ba0-115">PARAMETERS</span></span>

### <span data-ttu-id="c1ba0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ba0-116">-DefaultProfile</span></span>
<span data-ttu-id="c1ba0-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c1ba0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1ba0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c1ba0-118">-Name</span></span>
<span data-ttu-id="c1ba0-119">Specifica il nome del data factory su cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-119">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="c1ba0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1ba0-120">-ResourceGroupName</span></span>
<span data-ttu-id="c1ba0-121">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c1ba0-122">Questo cmdlet ottiene informazioni sulle fattorie di dati appartenenti al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c1ba0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ba0-123">CommonParameters</span></span>
<span data-ttu-id="c1ba0-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1ba0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ba0-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1ba0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ba0-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="c1ba0-126">INPUTS</span></span>

### <span data-ttu-id="c1ba0-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c1ba0-127">System.String</span></span>

## <span data-ttu-id="c1ba0-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1ba0-128">OUTPUTS</span></span>

### <span data-ttu-id="c1ba0-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c1ba0-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="c1ba0-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="c1ba0-130">NOTES</span></span>
* <span data-ttu-id="c1ba0-131">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="c1ba0-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c1ba0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1ba0-132">RELATED LINKS</span></span>

[<span data-ttu-id="c1ba0-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="c1ba0-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="c1ba0-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="c1ba0-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


