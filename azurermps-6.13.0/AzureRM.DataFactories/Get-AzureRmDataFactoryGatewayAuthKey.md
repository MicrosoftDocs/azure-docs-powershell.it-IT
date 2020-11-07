---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: b0855f8b30f057767643ebce39e5a78c69acc33e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686082"
---
# <span data-ttu-id="7d6c2-101">Get-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="7d6c2-101">Get-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="7d6c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d6c2-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6c2-103">Ottiene la chiave di autenticazione del gateway per una factory di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6c2-103">Gets gateway auth key for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d6c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d6c2-104">SYNTAX</span></span>

### <span data-ttu-id="7d6c2-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d6c2-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d6c2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7d6c2-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d6c2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d6c2-107">DESCRIPTION</span></span>
<span data-ttu-id="7d6c2-108">Il cmdlet **Get-AzureRmDataFactoryGatewayAuthKey** ottiene la chiave di autenticazione del gateway per un gateway di Azure Data Factory specificato.</span><span class="sxs-lookup"><span data-stu-id="7d6c2-108">The **Get-AzureRmDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="7d6c2-109">Il gateway viene registrato con un servizio cloud usando questo Key1 o Key2 di questa chiave auth.</span><span class="sxs-lookup"><span data-stu-id="7d6c2-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="7d6c2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d6c2-110">EXAMPLES</span></span>

### <span data-ttu-id="7d6c2-111">Esempio 1: ottiene la chiave AUTH di un gateway</span><span class="sxs-lookup"><span data-stu-id="7d6c2-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="7d6c2-112">Questo comando ottiene la chiave di autenticazione del gateway per il gateway di data factory denominato gateway.</span><span class="sxs-lookup"><span data-stu-id="7d6c2-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="7d6c2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d6c2-113">PARAMETERS</span></span>

### <span data-ttu-id="7d6c2-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="7d6c2-114">-DataFactoryName</span></span>
<span data-ttu-id="7d6c2-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="7d6c2-115">The data factory name.</span></span>

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

### <span data-ttu-id="7d6c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6c2-116">-DefaultProfile</span></span>
<span data-ttu-id="7d6c2-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7d6c2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d6c2-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="7d6c2-118">-GatewayName</span></span>
<span data-ttu-id="7d6c2-119">Nome del gateway di data factory.</span><span class="sxs-lookup"><span data-stu-id="7d6c2-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="7d6c2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d6c2-120">-InputObject</span></span>
<span data-ttu-id="7d6c2-121">Oggetto Data Factory</span><span class="sxs-lookup"><span data-stu-id="7d6c2-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6c2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d6c2-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d6c2-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7d6c2-123">The resource group name.</span></span>

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

### <span data-ttu-id="7d6c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6c2-124">CommonParameters</span></span>
<span data-ttu-id="7d6c2-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d6c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6c2-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d6c2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6c2-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d6c2-127">INPUTS</span></span>

### <span data-ttu-id="7d6c2-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7d6c2-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="7d6c2-129">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7d6c2-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7d6c2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7d6c2-130">System.String</span></span>

## <span data-ttu-id="7d6c2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d6c2-131">OUTPUTS</span></span>

### <span data-ttu-id="7d6c2-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="7d6c2-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="7d6c2-133">Note</span><span class="sxs-lookup"><span data-stu-id="7d6c2-133">NOTES</span></span>
* <span data-ttu-id="7d6c2-134">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="7d6c2-134">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7d6c2-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d6c2-135">RELATED LINKS</span></span>

<span data-ttu-id="7d6c2-136">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="7d6c2-136">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

