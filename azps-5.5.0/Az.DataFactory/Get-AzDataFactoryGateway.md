---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: 6d7b82a3046b56b473140b6830a0b04333cba9b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198894"
---
# <span data-ttu-id="09e3b-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="09e3b-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="09e3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="09e3b-103">Ottiene informazioni sui gateway logici in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="09e3b-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="09e3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09e3b-104">SYNTAX</span></span>

### <span data-ttu-id="09e3b-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="09e3b-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09e3b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="09e3b-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09e3b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="09e3b-107">DESCRIPTION</span></span>
<span data-ttu-id="09e3b-108">Il **cmdlet Get-AzDataFactoryGateway** ottiene informazioni sui gateway logici in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="09e3b-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="09e3b-109">Se si specifica il nome di un gateway, questo cmdlet ottiene informazioni sul gateway.</span><span class="sxs-lookup"><span data-stu-id="09e3b-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="09e3b-110">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i gateway per un data factory.</span><span class="sxs-lookup"><span data-stu-id="09e3b-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="09e3b-111">Se si vuole aggiungere un Microsoft SQL Server locale come servizio collegato a un data factory, è necessario installare un gateway nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="09e3b-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="09e3b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09e3b-112">EXAMPLES</span></span>

### <span data-ttu-id="09e3b-113">Esempio 1: Recuperare tutti i gateway logici in un data factory</span><span class="sxs-lookup"><span data-stu-id="09e3b-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
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

<span data-ttu-id="09e3b-114">Questo comando recupera informazioni su tutti i gateway logici per il data factory denominato WikiADF nel gruppo di risorse denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="09e3b-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="09e3b-115">Esempio 2: Ottenere un gateway logico specifico in un data factory</span><span class="sxs-lookup"><span data-stu-id="09e3b-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
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

<span data-ttu-id="09e3b-116">Questo comando recupera informazioni sul gateway logico denominato Gateway01 nel data factory denominato WikiADF nel gruppo di risorse denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="09e3b-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="09e3b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09e3b-117">PARAMETERS</span></span>

### <span data-ttu-id="09e3b-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="09e3b-118">-DataFactory</span></span>
<span data-ttu-id="09e3b-119">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="09e3b-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="09e3b-120">Questo cmdlet ottiene informazioni sui gateway logici nel data factory specificati da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="09e3b-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="09e3b-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="09e3b-121">-DataFactoryName</span></span>
<span data-ttu-id="09e3b-122">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="09e3b-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="09e3b-123">Questo cmdlet ottiene informazioni sui gateway logici nel data factory specificati da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="09e3b-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="09e3b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e3b-124">-DefaultProfile</span></span>
<span data-ttu-id="09e3b-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="09e3b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09e3b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="09e3b-126">-Name</span></span>
<span data-ttu-id="09e3b-127">Specifica il nome del gateway logico su cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="09e3b-127">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="09e3b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09e3b-128">-ResourceGroupName</span></span>
<span data-ttu-id="09e3b-129">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="09e3b-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="09e3b-130">Questo cmdlet ottiene informazioni sui gateway logici appartenenti al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="09e3b-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="09e3b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e3b-131">CommonParameters</span></span>
<span data-ttu-id="09e3b-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09e3b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e3b-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09e3b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e3b-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="09e3b-134">INPUTS</span></span>

### <span data-ttu-id="09e3b-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="09e3b-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="09e3b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="09e3b-136">System.String</span></span>

## <span data-ttu-id="09e3b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09e3b-137">OUTPUTS</span></span>

### <span data-ttu-id="09e3b-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="09e3b-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="09e3b-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="09e3b-139">NOTES</span></span>
* <span data-ttu-id="09e3b-140">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="09e3b-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="09e3b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09e3b-141">RELATED LINKS</span></span>

[<span data-ttu-id="09e3b-142">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="09e3b-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="09e3b-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="09e3b-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="09e3b-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="09e3b-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


