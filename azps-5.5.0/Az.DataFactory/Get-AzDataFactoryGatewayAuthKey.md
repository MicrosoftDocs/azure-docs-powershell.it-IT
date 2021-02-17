---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 8e86597292a9bcfef2163100d273d1e27daeb32a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186279"
---
# <span data-ttu-id="f648e-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="f648e-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="f648e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f648e-102">SYNOPSIS</span></span>
<span data-ttu-id="f648e-103">Ottiene la chiave di autenticazione del gateway per un Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="f648e-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="f648e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f648e-104">SYNTAX</span></span>

### <span data-ttu-id="f648e-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="f648e-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f648e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f648e-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f648e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f648e-107">DESCRIPTION</span></span>
<span data-ttu-id="f648e-108">Il cmdlet **Get-AzDataFactoryGatewayAuthKey ottiene** la chiave di autenticazione del gateway per un gateway di Data factory di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="f648e-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="f648e-109">Per registrare il gateway in un servizio cloud, usare questa chiave1 o chiave2 di questa chiave di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="f648e-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="f648e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f648e-110">EXAMPLES</span></span>

### <span data-ttu-id="f648e-111">Esempio 1: ottiene la chiave di autenticazione di un gateway</span><span class="sxs-lookup"><span data-stu-id="f648e-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="f648e-112">Questo comando recupera la chiave di autenticazione del gateway del data factory denominata MyGateway.</span><span class="sxs-lookup"><span data-stu-id="f648e-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="f648e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f648e-113">PARAMETERS</span></span>

### <span data-ttu-id="f648e-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f648e-114">-DataFactoryName</span></span>
<span data-ttu-id="f648e-115">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="f648e-115">The data factory name.</span></span>

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

### <span data-ttu-id="f648e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f648e-116">-DefaultProfile</span></span>
<span data-ttu-id="f648e-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f648e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f648e-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="f648e-118">-GatewayName</span></span>
<span data-ttu-id="f648e-119">Nome del gateway di data factory.</span><span class="sxs-lookup"><span data-stu-id="f648e-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="f648e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f648e-120">-InputObject</span></span>
<span data-ttu-id="f648e-121">Oggetto data factory</span><span class="sxs-lookup"><span data-stu-id="f648e-121">The data factory object</span></span>

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

### <span data-ttu-id="f648e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f648e-122">-ResourceGroupName</span></span>
<span data-ttu-id="f648e-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f648e-123">The resource group name.</span></span>

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

### <span data-ttu-id="f648e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f648e-124">CommonParameters</span></span>
<span data-ttu-id="f648e-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f648e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f648e-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f648e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f648e-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="f648e-127">INPUTS</span></span>

### <span data-ttu-id="f648e-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f648e-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f648e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f648e-129">System.String</span></span>

## <span data-ttu-id="f648e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f648e-130">OUTPUTS</span></span>

### <span data-ttu-id="f648e-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="f648e-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="f648e-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="f648e-132">NOTES</span></span>
* <span data-ttu-id="f648e-133">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="f648e-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f648e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f648e-134">RELATED LINKS</span></span>

<span data-ttu-id="f648e-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="f648e-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

