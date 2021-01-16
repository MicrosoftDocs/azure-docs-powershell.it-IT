---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: b9eebe26e64e9a7ce2497cdf9984ca6dabb062e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335524"
---
# <span data-ttu-id="41038-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="41038-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="41038-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41038-102">SYNOPSIS</span></span>
<span data-ttu-id="41038-103">Imposta la descrizione di un gateway in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="41038-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="41038-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41038-104">SYNTAX</span></span>

### <span data-ttu-id="41038-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41038-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41038-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="41038-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41038-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41038-107">DESCRIPTION</span></span>
<span data-ttu-id="41038-108">Il cmdlet **set-AzDataFactoryGateway** imposta la descrizione per il gateway specificato in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="41038-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="41038-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41038-109">EXAMPLES</span></span>

### <span data-ttu-id="41038-110">Esempio 1: impostare la descrizione di un gateway</span><span class="sxs-lookup"><span data-stu-id="41038-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="41038-111">Questo comando imposta la descrizione per il gateway denominato ContosoGateway nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="41038-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="41038-112">Il parametro Description specifica la nuova descrizione.</span><span class="sxs-lookup"><span data-stu-id="41038-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="41038-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41038-113">PARAMETERS</span></span>

### <span data-ttu-id="41038-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="41038-114">-DataFactory</span></span>
<span data-ttu-id="41038-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="41038-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="41038-116">Questo cmdlet imposta la descrizione del gateway nella Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="41038-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="41038-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="41038-117">-DataFactoryName</span></span>
<span data-ttu-id="41038-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="41038-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="41038-119">Questo cmdlet imposta la descrizione del gateway nella Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="41038-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="41038-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41038-120">-DefaultProfile</span></span>
<span data-ttu-id="41038-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="41038-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41038-122">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="41038-122">-Description</span></span>
<span data-ttu-id="41038-123">Specifica una descrizione per il gateway.</span><span class="sxs-lookup"><span data-stu-id="41038-123">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="41038-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="41038-124">-Name</span></span>
<span data-ttu-id="41038-125">Specifica il nome del gateway per cui impostare una descrizione.</span><span class="sxs-lookup"><span data-stu-id="41038-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="41038-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41038-126">-ResourceGroupName</span></span>
<span data-ttu-id="41038-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="41038-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="41038-128">Questo cmdlet imposta la descrizione di un gateway che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="41038-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="41038-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41038-129">CommonParameters</span></span>
<span data-ttu-id="41038-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41038-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41038-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41038-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41038-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41038-132">INPUTS</span></span>

### <span data-ttu-id="41038-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="41038-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="41038-134">System. String</span><span class="sxs-lookup"><span data-stu-id="41038-134">System.String</span></span>

## <span data-ttu-id="41038-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41038-135">OUTPUTS</span></span>

### <span data-ttu-id="41038-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="41038-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="41038-137">Note</span><span class="sxs-lookup"><span data-stu-id="41038-137">NOTES</span></span>
* <span data-ttu-id="41038-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="41038-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="41038-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41038-139">RELATED LINKS</span></span>

[<span data-ttu-id="41038-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="41038-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="41038-141">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="41038-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="41038-142">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="41038-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)


