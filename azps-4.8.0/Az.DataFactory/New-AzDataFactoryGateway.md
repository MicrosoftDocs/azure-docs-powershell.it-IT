---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: a4c755ab3f68eab2821807e7df6b9e24fad0df9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190284"
---
# <span data-ttu-id="315ce-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="315ce-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="315ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="315ce-102">SYNOPSIS</span></span>
<span data-ttu-id="315ce-103">Crea un gateway per una factory di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="315ce-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="315ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="315ce-104">SYNTAX</span></span>

### <span data-ttu-id="315ce-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="315ce-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="315ce-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="315ce-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="315ce-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="315ce-107">DESCRIPTION</span></span>
<span data-ttu-id="315ce-108">Il cmdlet **New-AzDataFactoryGateway** crea un gateway in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="315ce-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="315ce-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="315ce-109">EXAMPLES</span></span>

### <span data-ttu-id="315ce-110">Esempio 1: creare un gateway</span><span class="sxs-lookup"><span data-stu-id="315ce-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name              : ContosoGateway
Description       : my gateway
Version           : 
Status            : NeedRegistration
VersionStatus     : None
CreateTime        : 8/22/2014 1:40:34 AM
RegisterTime      : 
LastConnectTime   : 
ExpiryTime        : 
ProvisioningState : Succeeded
Key               : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="315ce-111">Questo comando crea un gateway denominato ContosoGateway nella data factory denominata WikiADF nel gruppo di risorse denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="315ce-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="315ce-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="315ce-112">PARAMETERS</span></span>

### <span data-ttu-id="315ce-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="315ce-113">-DataFactory</span></span>
<span data-ttu-id="315ce-114">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="315ce-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="315ce-115">Questo cmdlet crea un gateway per il Factory di dati specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="315ce-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="315ce-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="315ce-116">-DataFactoryName</span></span>
<span data-ttu-id="315ce-117">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="315ce-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="315ce-118">Questo cmdlet crea un gateway per il Factory di dati specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="315ce-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="315ce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="315ce-119">-DefaultProfile</span></span>
<span data-ttu-id="315ce-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="315ce-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="315ce-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="315ce-121">-Description</span></span>
<span data-ttu-id="315ce-122">Specifica una descrizione per il gateway.</span><span class="sxs-lookup"><span data-stu-id="315ce-122">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="315ce-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="315ce-123">-Name</span></span>
<span data-ttu-id="315ce-124">Specifica il nome del gateway da creare.</span><span class="sxs-lookup"><span data-stu-id="315ce-124">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="315ce-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="315ce-125">-ResourceGroupName</span></span>
<span data-ttu-id="315ce-126">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="315ce-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="315ce-127">Questo cmdlet crea un gateway che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="315ce-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="315ce-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="315ce-128">CommonParameters</span></span>
<span data-ttu-id="315ce-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="315ce-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="315ce-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="315ce-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="315ce-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="315ce-131">INPUTS</span></span>

### <span data-ttu-id="315ce-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="315ce-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="315ce-133">System. String</span><span class="sxs-lookup"><span data-stu-id="315ce-133">System.String</span></span>

## <span data-ttu-id="315ce-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="315ce-134">OUTPUTS</span></span>

### <span data-ttu-id="315ce-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="315ce-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="315ce-136">Note</span><span class="sxs-lookup"><span data-stu-id="315ce-136">NOTES</span></span>
* <span data-ttu-id="315ce-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="315ce-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="315ce-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="315ce-138">RELATED LINKS</span></span>

[<span data-ttu-id="315ce-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="315ce-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="315ce-140">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="315ce-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


