---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 5f59dfeeb024b4a81554a700bdcebc9d7f39e80a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196591"
---
# <span data-ttu-id="a9dfe-101">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="a9dfe-101">Get-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="a9dfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="a9dfe-103">Ottiene informazioni sui servizi collegati in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-103">Gets information about linked services in Azure Data Factory.</span></span>

## <span data-ttu-id="a9dfe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9dfe-104">SYNTAX</span></span>

### <span data-ttu-id="a9dfe-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="a9dfe-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9dfe-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a9dfe-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9dfe-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a9dfe-107">DESCRIPTION</span></span>
<span data-ttu-id="a9dfe-108">Il **cmdlet Get-AzDataFactoryLinkedService** ottiene informazioni sui servizi collegati in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-108">The **Get-AzDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="a9dfe-109">Se si specifica il nome di un servizio collegato, questo cmdlet ottiene informazioni sul servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="a9dfe-110">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i servizi collegati nel data factory.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="a9dfe-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9dfe-111">EXAMPLES</span></span>

### <span data-ttu-id="a9dfe-112">Esempio 1: Ottenere informazioni su tutti i servizi collegati</span><span class="sxs-lookup"><span data-stu-id="a9dfe-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="a9dfe-113">Questo comando recupera informazioni su tutti i servizi collegati nel data factory denominato WikiADF e quindi passa i servizi collegati al cmdlet Format-List usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a9dfe-114">Questo cmdlet formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="a9dfe-115">Per altre informazioni, digitare `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="a9dfe-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="a9dfe-116">Esempio 2: Ottenere informazioni su uno specifico servizio collegato</span><span class="sxs-lookup"><span data-stu-id="a9dfe-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="a9dfe-117">Questo comando recupera informazioni sul servizio collegato denominato HDILinkedService nel data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="a9dfe-118">Esempio 3: Ottenere informazioni su uno specifico servizio collegato specificando il parametro DataFactory</span><span class="sxs-lookup"><span data-stu-id="a9dfe-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="a9dfe-119">Il primo comando usa il cmdlet Get-AzDataFactory per ottenere il data factory denominato ContosoFactory e quindi lo archivia nella $DataFactory variabile.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-119">The first command uses the Get-AzDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="a9dfe-120">Il secondo comando riceve informazioni sul servizio collegato per il data factory archiviato in $DataFactory e quindi le passa al cmdlet Format-Table usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a9dfe-121">**Format-Table formatta** l'output come set di dati con le proprietà specificate come colonne del set di dati.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="a9dfe-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9dfe-122">PARAMETERS</span></span>

### <span data-ttu-id="a9dfe-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a9dfe-123">-DataFactory</span></span>
<span data-ttu-id="a9dfe-124">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="a9dfe-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a9dfe-125">Questo cmdlet ottiene servizi collegati che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a9dfe-126">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a9dfe-126">-DataFactoryName</span></span>
<span data-ttu-id="a9dfe-127">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a9dfe-128">Questo cmdlet ottiene servizi collegati che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a9dfe-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9dfe-129">-DefaultProfile</span></span>
<span data-ttu-id="a9dfe-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="a9dfe-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9dfe-131">-Name</span><span class="sxs-lookup"><span data-stu-id="a9dfe-131">-Name</span></span>
<span data-ttu-id="a9dfe-132">Specifica il nome del servizio collegato su cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-132">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="a9dfe-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9dfe-133">-ResourceGroupName</span></span>
<span data-ttu-id="a9dfe-134">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a9dfe-135">Questo cmdlet ottiene servizi collegati che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a9dfe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9dfe-136">CommonParameters</span></span>
<span data-ttu-id="a9dfe-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9dfe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9dfe-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9dfe-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9dfe-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="a9dfe-139">INPUTS</span></span>

### <span data-ttu-id="a9dfe-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a9dfe-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a9dfe-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a9dfe-141">System.String</span></span>

## <span data-ttu-id="a9dfe-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9dfe-142">OUTPUTS</span></span>

### <span data-ttu-id="a9dfe-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="a9dfe-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="a9dfe-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="a9dfe-144">NOTES</span></span>
* <span data-ttu-id="a9dfe-145">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="a9dfe-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a9dfe-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9dfe-146">RELATED LINKS</span></span>

[<span data-ttu-id="a9dfe-147">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="a9dfe-147">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)

[<span data-ttu-id="a9dfe-148">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="a9dfe-148">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


