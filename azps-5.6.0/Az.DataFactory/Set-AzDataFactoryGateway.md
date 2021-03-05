---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: c0cdd988c71a1943063fd7d07cd5e1b6d1c76f83
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998533"
---
# <span data-ttu-id="e3be8-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e3be8-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="e3be8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3be8-102">SYNOPSIS</span></span>
<span data-ttu-id="e3be8-103">Imposta la descrizione per un gateway in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3be8-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="e3be8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3be8-104">SYNTAX</span></span>

### <span data-ttu-id="e3be8-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="e3be8-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3be8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e3be8-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3be8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3be8-107">DESCRIPTION</span></span>
<span data-ttu-id="e3be8-108">Il cmdlet **Set-AzDataFactoryGateway** imposta la descrizione per il gateway specificato in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3be8-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="e3be8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3be8-109">EXAMPLES</span></span>

### <span data-ttu-id="e3be8-110">Esempio 1: Impostare la descrizione di un gateway</span><span class="sxs-lookup"><span data-stu-id="e3be8-110">Example 1: Set the description for a gateway</span></span>
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

<span data-ttu-id="e3be8-111">Questo comando imposta la descrizione del gateway denominato ContosoGateway nel data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e3be8-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="e3be8-112">Il parametro Description specifica la nuova descrizione.</span><span class="sxs-lookup"><span data-stu-id="e3be8-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="e3be8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3be8-113">PARAMETERS</span></span>

### <span data-ttu-id="e3be8-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3be8-114">-DataFactory</span></span>
<span data-ttu-id="e3be8-115">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="e3be8-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e3be8-116">Questo cmdlet imposta la descrizione del gateway nel data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e3be8-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e3be8-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e3be8-117">-DataFactoryName</span></span>
<span data-ttu-id="e3be8-118">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="e3be8-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e3be8-119">Questo cmdlet imposta la descrizione del gateway nel data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e3be8-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e3be8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3be8-120">-DefaultProfile</span></span>
<span data-ttu-id="e3be8-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e3be8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3be8-122">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3be8-122">-Description</span></span>
<span data-ttu-id="e3be8-123">Specifica una descrizione per il gateway.</span><span class="sxs-lookup"><span data-stu-id="e3be8-123">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="e3be8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e3be8-124">-Name</span></span>
<span data-ttu-id="e3be8-125">Specifica il nome del gateway per cui impostare una descrizione.</span><span class="sxs-lookup"><span data-stu-id="e3be8-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="e3be8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3be8-126">-ResourceGroupName</span></span>
<span data-ttu-id="e3be8-127">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3be8-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e3be8-128">Questo cmdlet imposta la descrizione di un gateway che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e3be8-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e3be8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3be8-129">CommonParameters</span></span>
<span data-ttu-id="e3be8-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3be8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3be8-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3be8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3be8-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3be8-132">INPUTS</span></span>

### <span data-ttu-id="e3be8-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e3be8-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="e3be8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e3be8-134">System.String</span></span>

## <span data-ttu-id="e3be8-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3be8-135">OUTPUTS</span></span>

### <span data-ttu-id="e3be8-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e3be8-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="e3be8-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3be8-137">NOTES</span></span>
* <span data-ttu-id="e3be8-138">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="e3be8-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e3be8-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3be8-139">RELATED LINKS</span></span>

[<span data-ttu-id="e3be8-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e3be8-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="e3be8-141">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e3be8-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="e3be8-142">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e3be8-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)


