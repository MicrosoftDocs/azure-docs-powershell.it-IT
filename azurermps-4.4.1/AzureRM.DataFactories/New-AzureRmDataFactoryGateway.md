---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 908c2b4804cf242642ce68adf0e28477fae40aac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516259"
---
# <span data-ttu-id="cb237-101">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="cb237-101">New-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="cb237-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb237-102">SYNOPSIS</span></span>
<span data-ttu-id="cb237-103">Crea un gateway per una factory di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="cb237-103">Creates a gateway for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb237-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb237-104">SYNTAX</span></span>

### <span data-ttu-id="cb237-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cb237-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb237-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cb237-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb237-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb237-107">DESCRIPTION</span></span>
<span data-ttu-id="cb237-108">Il cmdlet **New-AzureRmDataFactoryGateway** crea un gateway in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cb237-108">The **New-AzureRmDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="cb237-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb237-109">EXAMPLES</span></span>

### <span data-ttu-id="cb237-110">Esempio 1: creare un gateway</span><span class="sxs-lookup"><span data-stu-id="cb237-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="cb237-111">Questo comando crea un gateway denominato ContosoGateway nella data factory denominata WikiADF nel gruppo di risorse denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="cb237-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="cb237-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb237-112">PARAMETERS</span></span>

### <span data-ttu-id="cb237-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb237-113">-DataFactory</span></span>
<span data-ttu-id="cb237-114">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="cb237-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cb237-115">Questo cmdlet crea un gateway per il Factory di dati specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cb237-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb237-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="cb237-116">-DataFactoryName</span></span>
<span data-ttu-id="cb237-117">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="cb237-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cb237-118">Questo cmdlet crea un gateway per il Factory di dati specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cb237-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb237-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb237-119">-Description</span></span>
<span data-ttu-id="cb237-120">Specifica una descrizione per il gateway.</span><span class="sxs-lookup"><span data-stu-id="cb237-120">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="cb237-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb237-121">-Name</span></span>
<span data-ttu-id="cb237-122">Specifica il nome del gateway da creare.</span><span class="sxs-lookup"><span data-stu-id="cb237-122">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="cb237-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb237-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb237-124">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="cb237-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cb237-125">Questo cmdlet crea un gateway che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cb237-125">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb237-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb237-126">-DefaultProfile</span></span>
<span data-ttu-id="cb237-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb237-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb237-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb237-128">CommonParameters</span></span>
<span data-ttu-id="cb237-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb237-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb237-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb237-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb237-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb237-131">INPUTS</span></span>

## <span data-ttu-id="cb237-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb237-132">OUTPUTS</span></span>

### <span data-ttu-id="cb237-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="cb237-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="cb237-134">Note</span><span class="sxs-lookup"><span data-stu-id="cb237-134">NOTES</span></span>
* <span data-ttu-id="cb237-135">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="cb237-135">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cb237-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb237-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb237-137">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="cb237-137">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="cb237-138">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="cb237-138">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)

