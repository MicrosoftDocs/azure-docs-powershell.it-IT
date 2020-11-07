---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
ms.openlocfilehash: a90146480b0706d88f4ef7626b83008e08c22232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688346"
---
# <span data-ttu-id="d04a1-101">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d04a1-101">Get-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="d04a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d04a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d04a1-103">Ottiene informazioni sui gateway logici in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d04a1-103">Gets information about logical gateways in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d04a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d04a1-104">SYNTAX</span></span>

### <span data-ttu-id="d04a1-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d04a1-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d04a1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d04a1-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d04a1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d04a1-107">DESCRIPTION</span></span>
<span data-ttu-id="d04a1-108">Il cmdlet **Get-AzureRmDataFactoryGateway** ottiene informazioni sui gateway logici in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d04a1-108">The **Get-AzureRmDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="d04a1-109">Se specifichi il nome di un gateway, questo cmdlet ottiene le informazioni sul gateway.</span><span class="sxs-lookup"><span data-stu-id="d04a1-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="d04a1-110">Se non specifichi un nome, questo cmdlet ottiene informazioni su tutti i gateway per una data factory.</span><span class="sxs-lookup"><span data-stu-id="d04a1-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>

<span data-ttu-id="d04a1-111">Se si vuole aggiungere un Microsoft SQL Server locale come servizio collegato a una data factory, è necessario installare un gateway nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d04a1-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="d04a1-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d04a1-112">EXAMPLES</span></span>

### <span data-ttu-id="d04a1-113">Esempio 1: ottenere tutti i gateway logici in una data factory</span><span class="sxs-lookup"><span data-stu-id="d04a1-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
Name            : gateway1
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      : 
Name            : gateway2
Description     : 
Version         : 1.3.5338.1
Status          : Offline
VersionStatus   : UpToDate
CreateTime      : 8/29/2014 1:46:44 AM
RegisterTime    : 8/29/2014 1:48:36 AM
LastConnectTime : 8/29/2014 1:56:56 AM
ExpiryTime      :
```

<span data-ttu-id="d04a1-114">Questo comando consente di ottenere informazioni su tutti i gateway logici per la factory di dati denominata WikiADF nel gruppo di risorse denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="d04a1-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="d04a1-115">Esempio 2: ottenere un gateway logico specifico in una data factory</span><span class="sxs-lookup"><span data-stu-id="d04a1-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
Name            : Gateway01
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      :
```

<span data-ttu-id="d04a1-116">Questo comando consente di ottenere informazioni sul gateway logico denominato Gateway01 nella Factory di dati denominata WikiADF nel gruppo di risorse denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="d04a1-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="d04a1-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d04a1-117">PARAMETERS</span></span>

### <span data-ttu-id="d04a1-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d04a1-118">-DataFactory</span></span>
<span data-ttu-id="d04a1-119">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="d04a1-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d04a1-120">Questo cmdlet consente di ottenere informazioni sui gateway logici nella Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d04a1-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d04a1-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d04a1-121">-DataFactoryName</span></span>
<span data-ttu-id="d04a1-122">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="d04a1-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d04a1-123">Questo cmdlet consente di ottenere informazioni sui gateway logici nella Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d04a1-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d04a1-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d04a1-124">-Name</span></span>
<span data-ttu-id="d04a1-125">Specifica il nome del gateway logico su cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="d04a1-125">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="d04a1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d04a1-126">-ResourceGroupName</span></span>
<span data-ttu-id="d04a1-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="d04a1-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d04a1-128">Questo cmdlet consente di ottenere informazioni sui gateway logici che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d04a1-128">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d04a1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04a1-129">-DefaultProfile</span></span>
<span data-ttu-id="d04a1-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d04a1-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d04a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04a1-131">CommonParameters</span></span>
<span data-ttu-id="d04a1-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d04a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d04a1-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d04a1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04a1-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d04a1-134">INPUTS</span></span>

## <span data-ttu-id="d04a1-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d04a1-135">OUTPUTS</span></span>

### <span data-ttu-id="d04a1-136">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d04a1-136">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="d04a1-137">Note</span><span class="sxs-lookup"><span data-stu-id="d04a1-137">NOTES</span></span>
* <span data-ttu-id="d04a1-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="d04a1-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d04a1-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d04a1-139">RELATED LINKS</span></span>

[<span data-ttu-id="d04a1-140">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d04a1-140">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="d04a1-141">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d04a1-141">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="d04a1-142">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d04a1-142">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


