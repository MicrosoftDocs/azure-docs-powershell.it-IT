---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 2cca641538be35f18173fd1e03b5f593c87649bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511251"
---
# <span data-ttu-id="67541-101">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="67541-101">Set-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="67541-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67541-102">SYNOPSIS</span></span>
<span data-ttu-id="67541-103">Imposta la descrizione di un gateway in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="67541-103">Sets the description for a gateway in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67541-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67541-104">SYNTAX</span></span>

### <span data-ttu-id="67541-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67541-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67541-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="67541-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67541-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67541-107">DESCRIPTION</span></span>
<span data-ttu-id="67541-108">Il cmdlet **set-AzureRmDataFactoryGateway** imposta la descrizione per il gateway specificato in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="67541-108">The **Set-AzureRmDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="67541-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67541-109">EXAMPLES</span></span>

### <span data-ttu-id="67541-110">Esempio 1: impostare la descrizione di un gateway</span><span class="sxs-lookup"><span data-stu-id="67541-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="67541-111">Questo comando imposta la descrizione per il gateway denominato ContosoGateway nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="67541-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="67541-112">Il parametro Description specifica la nuova descrizione.</span><span class="sxs-lookup"><span data-stu-id="67541-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="67541-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67541-113">PARAMETERS</span></span>

### <span data-ttu-id="67541-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="67541-114">-DataFactory</span></span>
<span data-ttu-id="67541-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="67541-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="67541-116">Questo cmdlet imposta la descrizione del gateway nella Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="67541-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="67541-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="67541-117">-DataFactoryName</span></span>
<span data-ttu-id="67541-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="67541-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="67541-119">Questo cmdlet imposta la descrizione del gateway nella Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="67541-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="67541-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="67541-120">-Description</span></span>
<span data-ttu-id="67541-121">Specifica una descrizione per il gateway.</span><span class="sxs-lookup"><span data-stu-id="67541-121">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67541-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="67541-122">-Name</span></span>
<span data-ttu-id="67541-123">Specifica il nome del gateway per cui impostare una descrizione.</span><span class="sxs-lookup"><span data-stu-id="67541-123">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="67541-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67541-124">-ResourceGroupName</span></span>
<span data-ttu-id="67541-125">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="67541-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="67541-126">Questo cmdlet imposta la descrizione di un gateway che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="67541-126">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="67541-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67541-127">-DefaultProfile</span></span>
<span data-ttu-id="67541-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67541-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67541-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67541-129">CommonParameters</span></span>
<span data-ttu-id="67541-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67541-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67541-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67541-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67541-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67541-132">INPUTS</span></span>

## <span data-ttu-id="67541-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67541-133">OUTPUTS</span></span>

### <span data-ttu-id="67541-134">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="67541-134">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="67541-135">Note</span><span class="sxs-lookup"><span data-stu-id="67541-135">NOTES</span></span>
* <span data-ttu-id="67541-136">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="67541-136">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="67541-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67541-137">RELATED LINKS</span></span>

[<span data-ttu-id="67541-138">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="67541-138">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="67541-139">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="67541-139">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="67541-140">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="67541-140">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)


