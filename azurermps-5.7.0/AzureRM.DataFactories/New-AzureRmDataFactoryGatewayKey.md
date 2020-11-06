---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: d360a468d69306b5f203cbd28d17e9bfcc00bdcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509932"
---
# <span data-ttu-id="6363b-101">New-AzureRmDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="6363b-101">New-AzureRmDataFactoryGatewayKey</span></span>

## <span data-ttu-id="6363b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6363b-102">SYNOPSIS</span></span>
<span data-ttu-id="6363b-103">Crea una chiave del gateway per una factory di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="6363b-103">Creates a gateway key for an Azure Data Factory.</span></span> <span data-ttu-id="6363b-104">Questo cmdlet è deprecato e dovresti usare invece **New-AzureRmDataFactoryGatewayAuthKey** .</span><span class="sxs-lookup"><span data-stu-id="6363b-104">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6363b-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6363b-105">SYNTAX</span></span>

### <span data-ttu-id="6363b-106">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6363b-106">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6363b-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6363b-107">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6363b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6363b-108">DESCRIPTION</span></span>
<span data-ttu-id="6363b-109">Il cmdlet **New-AzureRmDataFactoryGatewayKey** crea una chiave del gateway per un gateway di Azure Data Factory specificato.</span><span class="sxs-lookup"><span data-stu-id="6363b-109">The **New-AzureRmDataFactoryGatewayKey** cmdlet creates a gateway key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="6363b-110">Il gateway viene registrato con un servizio cloud usando questa chiave.</span><span class="sxs-lookup"><span data-stu-id="6363b-110">You register the gateway with a cloud service by using this key.</span></span> <span data-ttu-id="6363b-111">Questo cmdlet è deprecato e dovresti usare invece **New-AzureRmDataFactoryGatewayAuthKey** .</span><span class="sxs-lookup"><span data-stu-id="6363b-111">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

## <span data-ttu-id="6363b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6363b-112">EXAMPLES</span></span>

### <span data-ttu-id="6363b-113">Esempio 1: creare una chiave gateway</span><span class="sxs-lookup"><span data-stu-id="6363b-113">Example 1: Create a gateway key</span></span>
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="6363b-114">Questo comando crea una chiave del gateway per il gateway di data factory denominata ContosoGateway e quindi passa la chiave del gateway al cmdlet Format-List usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="6363b-114">This command creates a gateway key for the data factory gateway named ContosoGateway, and then passes the gateway key to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6363b-115">Per altre informazioni, digitare `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="6363b-115">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="6363b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6363b-116">PARAMETERS</span></span>

### <span data-ttu-id="6363b-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6363b-117">-DataFactory</span></span>
<span data-ttu-id="6363b-118">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="6363b-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6363b-119">Questo cmdlet crea una chiave del gateway per la factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6363b-119">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6363b-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6363b-120">-DataFactoryName</span></span>
<span data-ttu-id="6363b-121">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="6363b-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6363b-122">Questo cmdlet crea una chiave del gateway per la factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6363b-122">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6363b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6363b-123">-DefaultProfile</span></span>
<span data-ttu-id="6363b-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6363b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6363b-125">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="6363b-125">-GatewayName</span></span>
<span data-ttu-id="6363b-126">Specifica il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="6363b-126">Specifies the name of the gateway.</span></span>
<span data-ttu-id="6363b-127">Questo cmdlet crea una chiave per il gateway specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6363b-127">This cmdlet creates a key for the gateway that this parameter specifies.</span></span>

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

### <span data-ttu-id="6363b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6363b-128">-ResourceGroupName</span></span>
<span data-ttu-id="6363b-129">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="6363b-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6363b-130">Questo cmdlet crea una chiave per un gateway che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6363b-130">This cmdlet creates a key for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6363b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6363b-131">CommonParameters</span></span>
<span data-ttu-id="6363b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6363b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6363b-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6363b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6363b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6363b-134">INPUTS</span></span>

### <span data-ttu-id="6363b-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6363b-135">None</span></span>
<span data-ttu-id="6363b-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6363b-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6363b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6363b-137">OUTPUTS</span></span>

### <span data-ttu-id="6363b-138">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="6363b-138">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span></span>

## <span data-ttu-id="6363b-139">Note</span><span class="sxs-lookup"><span data-stu-id="6363b-139">NOTES</span></span>
* <span data-ttu-id="6363b-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="6363b-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6363b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6363b-141">RELATED LINKS</span></span>

<span data-ttu-id="6363b-142">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
 [New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="6363b-142">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>


