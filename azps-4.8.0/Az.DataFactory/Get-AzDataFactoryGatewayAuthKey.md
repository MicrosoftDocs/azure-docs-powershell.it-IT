---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 8e86597292a9bcfef2163100d273d1e27daeb32a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190491"
---
# <span data-ttu-id="81eb7-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="81eb7-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="81eb7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="81eb7-103">Ottiene la chiave di autenticazione del gateway per una factory di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="81eb7-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="81eb7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81eb7-104">SYNTAX</span></span>

### <span data-ttu-id="81eb7-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="81eb7-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81eb7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="81eb7-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81eb7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81eb7-107">DESCRIPTION</span></span>
<span data-ttu-id="81eb7-108">Il cmdlet **Get-AzDataFactoryGatewayAuthKey** ottiene la chiave di autenticazione del gateway per un gateway di Azure Data Factory specificato.</span><span class="sxs-lookup"><span data-stu-id="81eb7-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="81eb7-109">Il gateway viene registrato con un servizio cloud usando questo Key1 o Key2 di questa chiave auth.</span><span class="sxs-lookup"><span data-stu-id="81eb7-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="81eb7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81eb7-110">EXAMPLES</span></span>

### <span data-ttu-id="81eb7-111">Esempio 1: ottiene la chiave AUTH di un gateway</span><span class="sxs-lookup"><span data-stu-id="81eb7-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="81eb7-112">Questo comando ottiene la chiave di autenticazione del gateway per il gateway di data factory denominato gateway.</span><span class="sxs-lookup"><span data-stu-id="81eb7-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="81eb7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81eb7-113">PARAMETERS</span></span>

### <span data-ttu-id="81eb7-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="81eb7-114">-DataFactoryName</span></span>
<span data-ttu-id="81eb7-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="81eb7-115">The data factory name.</span></span>

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

### <span data-ttu-id="81eb7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81eb7-116">-DefaultProfile</span></span>
<span data-ttu-id="81eb7-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="81eb7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81eb7-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="81eb7-118">-GatewayName</span></span>
<span data-ttu-id="81eb7-119">Nome del gateway di data factory.</span><span class="sxs-lookup"><span data-stu-id="81eb7-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="81eb7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81eb7-120">-InputObject</span></span>
<span data-ttu-id="81eb7-121">Oggetto Data Factory</span><span class="sxs-lookup"><span data-stu-id="81eb7-121">The data factory object</span></span>

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

### <span data-ttu-id="81eb7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81eb7-122">-ResourceGroupName</span></span>
<span data-ttu-id="81eb7-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="81eb7-123">The resource group name.</span></span>

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

### <span data-ttu-id="81eb7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81eb7-124">CommonParameters</span></span>
<span data-ttu-id="81eb7-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81eb7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81eb7-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81eb7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81eb7-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81eb7-127">INPUTS</span></span>

### <span data-ttu-id="81eb7-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="81eb7-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="81eb7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="81eb7-129">System.String</span></span>

## <span data-ttu-id="81eb7-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81eb7-130">OUTPUTS</span></span>

### <span data-ttu-id="81eb7-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="81eb7-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="81eb7-132">Note</span><span class="sxs-lookup"><span data-stu-id="81eb7-132">NOTES</span></span>
* <span data-ttu-id="81eb7-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="81eb7-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="81eb7-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81eb7-134">RELATED LINKS</span></span>

<span data-ttu-id="81eb7-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="81eb7-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

